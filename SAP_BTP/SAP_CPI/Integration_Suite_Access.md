# Access SAP Integration Suite

This guide explains how to assign the required role collections and resolve unauthorized issue when accessing SAP Integration Suite.

---

## Issue

After subscribing to SAP Integration Suite and clicking **Go to Application**, users may encounter authorization errors

```text
https://<global-account-name>.integrationsuite-trial.cfapps.ap21.hana.ondemand.com
```

---

## Step 1: Open Integration Suite

Navigate to:

Services → Instances and Subscriptions

Select **Integration Suite** and click **Go to Application**.

---

## Step 2: Integration Provisioner Page

The Integration Provisioner application may open while SAP prepares the Integration Suite environment.

Wait until provisioning activities are completed.

![Integration Provisioner](Images/integration_provisioner.png)

---

## Step 3: Missing Role Collection

If required role collections are not assigned, some capabilities will not be visible.

A message similar to the following may appear.

![Missing Role](Images/missing_role.png)

---

## Step 4: Assign Required Role Collections

Navigate to:

Security → Users

Select your user ID.

Choose **Assign Role Collection**.

Assign all available Integration Suite role collections.

Common examples include:

- Integration_Provisioner
- PI_Integrator_Group
- AuthGroup_IntegrationDeveloper
- APIManagement.Administrator

Role collections available may vary depending on the tenant version.

-role assignment, verify that the user now has the required Integration Suite permissions.

Images/updated_role_collection.png

---

## Step 6: Reopen Integration Suite

Log out and log in again.

Launch Integration Suite once more.

If access was previously denied, the authorization error should no longer appear.

Images/unauthorized_error_cpi.png

---

## Result

The required role collections have been assigned successfully.

You should now be able to:

- Access Integration Suite
- Open Cloud Integration capabilities
- Create Packages
- Create and Deploy iFlows
- Manage APIs and other Integration Suite services
