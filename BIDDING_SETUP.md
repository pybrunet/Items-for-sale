# Public Google Sheet Bidding System Setup

## Step 1: Create Your Bidding Google Sheet

1. Go to [Google Sheets](https://sheets.google.com)
2. Create a new blank spreadsheet
3. Name it "Live Bidding - Items for Sale"

## Step 2: Set Up Your Sheet Columns

Create these column headers in Row 1:

| A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|
| **Timestamp** | **Item Name** | **Bidder Name** | **Bid Amount** | **Contact Info** | **Notes** | **Status** |

## Step 3: Add Example Data (Optional)

Add some sample bids to show how it works:

```
Row 2: [Auto] | Area Rug | John D. | $485.00 | john@email.com | Beautiful rug! | Active
Row 3: [Auto] | Dyson Air Purifier | Sarah M. | $410.00 | 305-xxx-xxxx | Need by weekend | Active
Row 4: [Auto] | Car Seat | Mike R. | $140.00 | mike.r@email.com | Local pickup preferred | Active
```

## Step 4: Make Sheet Public

1. Click the **"Share"** button (top right)
2. Click **"Change to anyone with the link"**
3. Set permissions to **"Viewer"** (so people can see bids but not edit)
4. Copy the share link - it will look like:
   `https://docs.google.com/spreadsheets/d/1ABC123XYZ789.../edit#gid=0`

## Step 5: Update Your Landing Page

1. Open `index.html`
2. Find both instances of `YOUR_SHEET_ID_HERE`
3. Replace with your actual Sheet ID (the long string between `/d/` and `/edit`)

**Example:**
If your sheet URL is:
`https://docs.google.com/spreadsheets/d/1ABC123XYZ789DEF456/edit#gid=0`

Your Sheet ID is: `1ABC123XYZ789DEF456`

## Step 6: Create a Bid Submission Process

### Option A: Simple Email Process
- Buyers email you their bids
- You manually add them to the sheet
- Update the current bid amounts on your landing page

### Option B: Google Form + Auto-populate
1. Create a Google Form that feeds into your sheet
2. Link the "Place Your Bid" buttons to the form
3. Form responses automatically appear in your sheet

## Step 7: Sheet Formatting (Recommended)

1. **Freeze the header row**: Select row 1 → View → Freeze → 1 row
2. **Sort by timestamp**: Data → Sort range → Sort by Timestamp (newest first)
3. **Add conditional formatting**: 
   - Highlight highest bid for each item in green
   - Color-code by item type
4. **Auto-timestamp**: Use `=NOW()` formula in timestamp column

## Step 8: Promote Transparency

Add this text to your landing page or emails:
*"All bids are publicly visible on our live bidding sheet. See real-time competition and be the highest bidder!"*

## Tips for Success

✅ **Update regularly** - Keep current bids on landing page in sync with sheet  
✅ **Set bidding deadlines** - Create urgency with clear end times  
✅ **Respond quickly** - Confirm bids via email/WhatsApp  
✅ **Show activity** - Regular updates encourage more bidding  
✅ **Be transparent** - Public process builds trust  

## Security Notes

- Sheet is view-only for public
- Only you can edit bid information
- Consider using a separate Gmail account for this sheet
- Monitor for any inappropriate content in bids

---

**Your public bidding sheet will create a competitive auction atmosphere and likely drive higher final prices!** 