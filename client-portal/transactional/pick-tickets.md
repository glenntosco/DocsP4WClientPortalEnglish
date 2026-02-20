# Pick Tickets

A Pick Ticket is the operational document that instructs the 3PL which products to pick from inventory to fulfil an outbound order. Navigate to **Transactional → Pick Tickets** to access this section.

Pick Tickets can be created **manually** or loaded in bulk via **import**.

> 📷 Screenshot: Pick Tickets list screen with New and Import buttons.

---

## Manual Creation

> 📷 Video reference: Step-by-step walkthrough for creating a Pick Ticket manually (`PickTickets manual.mp4`).

### Step by Step

1. Click **New**. A window will appear — select the **client** and the **warehouse**.

> 📷 Screenshot: New Pick Ticket window with client and warehouse selectors.

2. The ticket detail screen will open. Fill in:
   - **Shipping details**
   - **Comments** and any additional information
   - **Product lines** — add each item to be dispatched (this is the most important step)
3. **Release the order** once all product lines have been added.

> 📷 Screenshot: Pick Ticket detail screen showing product lines, shipping fields, and the Release button.

### After Release

- The order appears in the list with the status **"Unallocated"**, indicating it has not yet been assigned or worked by the 3PL.

{% hint style="danger" %}
Once a Pick Ticket is in **Unallocated** status, it cannot be deleted or modified by the client. Changes are only possible if the 3PL returns the order to **Draft** status. Until then, the client can only view the order's status.
{% endhint %}

> 📷 Screenshot: Pick Ticket list showing an order in Unallocated status.

---

## Import (Bulk Creation)

> 📷 Video reference: Step-by-step walkthrough for creating Pick Tickets by bulk import (`PickTickets creada por importación.mp4`).

### Step by Step

1. Go to **Transactional → Pick Tickets** and click **Import** (top right).
2. The system will immediately open a file browser — select your Excel file.

> 📷 Screenshot: File browser opened for selecting the import file.

3. After selecting the file, a confirmation message will appear — validate the import.

> 📷 Screenshot: Import confirmation dialog.

4. Imported orders are created in **Draft** status. Open each order and **release** it for the 3PL to process.

> 📷 Screenshot: Pick Ticket list showing imported orders in Draft status.

{% hint style="warning" %}
Imported orders remain in Draft until manually released. Any modification is only possible if the 3PL returns the order to Draft status.
{% endhint %}

---

**Related:** [Purchase Orders](purchase-orders.md) · [Clients](../master-data/clients.md) · [Reports](../reports/README.md)
