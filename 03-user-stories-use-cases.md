User Stories

As an employee, I want to see my remaining leave balance, so that I know if I have leaves left or not.
As a manager, I want to be notified of my employee's leave request, so that I can approve or decline it.
As HR, I want to see all employees' leave requests, so that I can approve or decline them.

Use Case: Submit Leave Request

Actor: Employee

Preconditions:

Employee has an account on the system.
HR has already recorded the employee's initial leave balance in the system.

Main Flow:

Employee opens the app and submits a leave request → status: Pending Manager Approval
System checks manager's status: if Available, request goes to manager; if On Leave, request routes automatically to Delegate Approver
If balance is insufficient, system shows a warning that the leave will be deducted as unpaid; employee chooses to proceed or cancel
Manager (or Delegate) approves the request → status changes to Pending HR Approval
HR reviews the balance and gives final approval → status changes to Approved
Employee receives a notification with the final status

Alternative Flow (Decline):

Manager (or Delegate) declines the request → status changes to Declined
Request does not proceed to HR
Employee receives a decline notification

Postcondition: Employee's leave balance is updated automatically, and the request is logged for Employee, Manager, and HR.
