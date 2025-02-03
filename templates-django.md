```markdown
# **Django Templates & Views - Key Notes**

## **1. Views & Templates Overview**
- **Views:** Handle Python code, merge data from models/templates, and generate HTTP responses.  
- **Templates:** Mostly HTML with placeholders (hotspots) for dynamic content. They simplify user interface creation.  
- **Purpose:** Replace complex string concatenation in views with clean, dynamic HTML rendering.  

## **2. Request-Response Cycle**
- The cycle remains the same:  
  **Request → Process in View → Render Template → Response to Browser**  
- Instead of manually concatenating strings, Django uses a **template engine** for cleaner code.  

## **3. Template Engine Basics**
- Django’s built-in template engine renders HTML dynamically.  
- Templates include static HTML with dynamic **placeholders** for data.  
- **Context:** A dictionary of key-value pairs passed from views to templates for data substitution.  

## **4. Syntax in Templates**
- **Double Curly Braces `{{ }}`:** Insert variables (e.g., `{{ guess }}` renders the value of `guess`).  
- **Curly Brace with Percent `{% %}`:** Add logic like conditionals and loops (e.g., `if`, `else`, `for`).  

### Example:
```django
{% if guess < 42 %}
  Too Low
{% elif guess > 42 %}
  Too High
{% else %}
  Just Right
{% endif %}
```  
- This approach keeps Python logic out of raw HTML for better readability.

## **5. Context & Rendering Example**
### **View Code Example:**
```python
context = {'guess': 200}
return render(request, 'app_name/template.html', context)
```  

### **Template Example:**
```html
Your guess was {{ guess }}
```  

### **Result:**
```
Your guess was 200
```

## **6. Template Naming Conventions**
- **Global Template Issue:** Django treats template names as global, causing conflicts.  
- **Solution:**  
  - Organize templates using subfolders named after applications.  
  - Format: `templates/app_name/detail.html`  
- Ensures clarity and avoids naming conflicts in large projects.  

## **7. Template Reusability**
- Templates can be accessed across different apps.  
- Common practice: Prefix template names with the app name to maintain consistency.  

## **8. Django Project Structure**
- A **Django Project** consists of multiple **applications**.  
- Templates are shared globally, so proper folder structure and naming conventions are critical.  
```
