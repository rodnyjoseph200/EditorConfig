# .NET EditorConfig

>## Welcome
>The .editorconfig file provided in this repo contains opinionated settings. Feel free to use as is or update to your liking.

>For descriptions and examples of the rules in the editor config, see below \
(Includes Table of Content)

---

<details>

<summary><h2> Table of Content </h2></summary>

- [1. indent_size](#1-indent_size)
- [2. indent_style](#2-indent_style)
- [3. tab_width](#3-tab_width)
- [4. end_of_line](#4-end_of_line)
- [5. insert_final_newline](#5-insert_final_newline)
- [6. dotnet_separate_import_directive_groups](#6-dotnet_separate_import_directive_groups)
- [7. dotnet_sort_system_directives_first](#7-dotnet_sort_system_directives_first)
- [8. file_header_template](#8-file_header_template)
- [9. dotnet_style_qualification_for_event](#9-dotnet_style_qualification_for_event)
- [10. dotnet_style_qualification_for_field](#10-dotnet_style_qualification_for_field)
- [11. dotnet_style_qualification_for_method](#11-dotnet_style_qualification_for_method)
- [12. dotnet_style_qualification_for_property](#12-dotnet_style_qualification_for_property)
- [13. dotnet_style_predefined_type_for_locals_parameters_members](#13-dotnet_style_predefined_type_for_locals_parameters_members)
- [14. dotnet_style_predefined_type_for_member_access](#14-dotnet_style_predefined_type_for_member_access)
- [15. dotnet_style_parentheses_in_arithmetic_binary_operators](#15-dotnet_style_parentheses_in_arithmetic_binary_operators)
- [16. dotnet_style_parentheses_in_other_binary_operators](#16-dotnet_style_parentheses_in_other_binary_operators)
- [17. dotnet_style_parentheses_in_other_operators](#17-dotnet_style_parentheses_in_other_operators)
- [18. dotnet_style_parentheses_in_relational_binary_operators](#18-dotnet_style_parentheses_in_relational_binary_operators)
- [19. dotnet_style_require_accessibility_modifiers](#19-dotnet_style_require_accessibility_modifiers)
- [20. dotnet_style_coalesce_expression](#20-dotnet_style_coalesce_expression)
- [21. dotnet_style_collection_initializer](#21-dotnet_style_collection_initializer)
- [22. dotnet_style_explicit_tuple_names](#22-dotnet_style_explicit_tuple_names)
- [23. dotnet_style_namespace_match_folder](#23-dotnet_style_namespace_match_folder)
- [24. dotnet_style_null_propagation](#24-dotnet_style_null_propagation)
- [25. dotnet_style_object_initializer](#25-dotnet_style_object_initializer)
- [26. dotnet_style_operator_placement_when_wrapping](#26-dotnet_style_operator_placement_when_wrapping)
- [27. dotnet_style_prefer_auto_properties](#27-dotnet_style_prefer_auto_properties)
- [28. dotnet_style_prefer_collection_expression](#28-dotnet_style_prefer_collection_expression)
- [29. dotnet_style_prefer_compound_assignment](#29-dotnet_style_prefer_compound_assignment)
- [30. dotnet_style_prefer_conditional_expression_over_assignment](#30-dotnet_style_prefer_conditional_expression_over_assignment)
- [31. dotnet_style_prefer_conditional_expression_over_return](#31-dotnet_style_prefer_conditional_expression_over_return)
- [32. dotnet_style_prefer_foreach_explicit_cast_in_source](#32-dotnet_style_prefer_foreach_explicit_cast_in_source)
- [33. dotnet_style_prefer_inferred_anonymous_type_member_names](#33-dotnet_style_prefer_inferred_anonymous_type_member_names)
- [34. dotnet_style_prefer_inferred_tuple_names](#34-dotnet_style_prefer_inferred_tuple_names)
- [35. dotnet_style_prefer_is_null_check_over_reference_equality_method](#35-dotnet_style_prefer_is_null_check_over_reference_equality_method)
- [36. dotnet_style_prefer_simplified_boolean_expressions](#36-dotnet_style_prefer_simplified_boolean_expressions)
- [37. dotnet_style_prefer_simplified_interpolation](#37-dotnet_style_prefer_simplified_interpolation)
- [38. dotnet_style_readonly_field](#38-dotnet_style_readonly_field)
- [39. dotnet_code_quality_unused_parameters](#39-dotnet_code_quality_unused_parameters)
- [40. dotnet_remove_unnecessary_suppression_exclusions](#40-dotnet_remove_unnecessary_suppression_exclusions)
- [41. dotnet_style_allow_multiple_blank_lines_experimental](#41-dotnet_style_allow_multiple_blank_lines_experimental)
- [42. dotnet_style_allow_statement_immediately_after_block_experimental](#42-dotnet_style_allow_statement_immediately_after_block_experimental)
- [43. csharp_style_var_elsewhere](#43-csharp_style_var_elsewhere)
- [44. csharp_style_var_for_built_in_types](#44-csharp_style_var_for_built_in_types)
- [45. csharp_style_var_when_type_is_apparent](#45-csharp_style_var_when_type_is_apparent)
- [46. csharp_style_expression_bodied_accessors](#46-csharp_style_expression_bodied_accessors)
- [47. csharp_style_expression_bodied_constructors](#47-csharp_style_expression_bodied_constructors)
- [48. csharp_style_expression_bodied_indexers](#48-csharp_style_expression_bodied_indexers)
- [49. csharp_style_expression_bodied_lambdas](#49-csharp_style_expression_bodied_lambdas)
- [50. csharp_style_expression_bodied_local_functions](#50-csharp_style_expression_bodied_local_functions)
- [51. csharp_style_expression_bodied_methods](#51-csharp_style_expression_bodied_methods)
- [52. csharp_style_expression_bodied_operators](#52-csharp_style_expression_bodied_operators)
- [53. csharp_style_expression_bodied_properties](#53-csharp_style_expression_bodied_properties)
- [54. csharp_style_pattern_matching_over_as_with_null_check](#54-csharp_style_pattern_matching_over_as_with_null_check)
- [55. csharp_style_pattern_matching_over_is_with_cast_check](#55-csharp_style_pattern_matching_over_is_with_cast_check)
- [56. csharp_style_prefer_extended_property_pattern](#56-csharp_style_prefer_extended_property_pattern)
- [57. csharp_style_prefer_not_pattern](#57-csharp_style_prefer_not_pattern)
- [58. csharp_style_prefer_pattern_matching](#58-csharp_style_prefer_pattern_matching)
- [59. csharp_style_prefer_switch_expression](#59-csharp_style_prefer_switch_expression)
- [60. csharp_style_conditional_delegate_call](#60-csharp_style_conditional_delegate_call)
- [61. csharp_prefer_static_anonymous_function](#61-csharp_prefer_static_anonymous_function)
- [62. csharp_prefer_static_local_function](#62-csharp_prefer_static_local_function)
- [63. csharp_preferred_modifier_order](#63-csharp_preferred_modifier_order)
- [64. csharp_style_prefer_readonly_struct](#64-csharp_style_prefer_readonly_struct)
- [65. csharp_style_prefer_readonly_struct_member](#65-csharp_style_prefer_readonly_struct_member)
- [66. csharp_prefer_braces](#66-csharp_prefer_braces)
- [67. csharp_prefer_simple_using_statement](#67-csharp_prefer_simple_using_statement)
- [68. csharp_style_namespace_declarations](#68-csharp_style_namespace_declarations)
- [69. csharp_style_prefer_method_group_conversion](#69-csharp_style_prefer_method_group_conversion)
- [70. csharp_style_prefer_primary_constructors](#70-csharp_style_prefer_primary_constructors)
- [71. csharp_style_prefer_top_level_statements](#71-csharp_style_prefer_top_level_statements)
- [72. csharp_prefer_simple_default_expression](#72-csharp_prefer_simple_default_expression)
- [73. csharp_style_deconstructed_variable_declaration](#73-csharp_style_deconstructed_variable_declaration)
- [74. csharp_style_implicit_object_creation_when_type_is_apparent](#74-csharp_style_implicit_object_creation_when_type_is_apparent)
- [75. csharp_style_inlined_variable_declaration](#75-csharp_style_inlined_variable_declaration)
- [76. csharp_style_prefer_index_operator](#76-csharp_style_prefer_index_operator)
- [77. csharp_style_prefer_local_over_anonymous_function](#77-csharp_style_prefer_local_over_anonymous_function)
- [78. csharp_style_prefer_null_check_over_type_check](#78-csharp_style_prefer_null_check_over_type_check)
- [79. csharp_style_prefer_range_operator](#79-csharp_style_prefer_range_operator)
- [80. csharp_style_prefer_tuple_swap](#80-csharp_style_prefer_tuple_swap)
- [81. csharp_style_prefer_utf8_string_literals](#81-csharp_style_prefer_utf8_string_literals)
- [82. csharp_style_throw_expression](#82-csharp_style_throw_expression)
- [83. csharp_style_unused_value_assignment_preference](#83-csharp_style_unused_value_assignment_preference)
- [84. csharp_style_unused_value_expression_statement_preference](#84-csharp_style_unused_value_expression_statement_preference)
- [85. csharp_using_directive_placement](#85-csharp_using_directive_placement)
- [86. csharp_style_allow_blank_line_after_colon_in_constructor_initializer_experimental](#86-csharp_style_allow_blank_line_after_colon_in_constructor_initializer_experimental)
- [87. csharp_style_allow_blank_line_after_token_in_arrow_expression_clause_experimental](#87-csharp_style_allow_blank_line_after_token_in_arrow_expression_clause_experimental)
- [88. csharp_style_allow_blank_line_after_token_in_conditional_expression_experimental](#88-csharp_style_allow_blank_line_after_token_in_conditional_expression_experimental)
- [89. csharp_style_allow_blank_lines_between_consecutive_braces_experimental](#89-csharp_style_allow_blank_lines_between_consecutive_braces_experimental)
- [90. csharp_style_allow_embedded_statements_on_same_line_experimental](#90-csharp_style_allow_embedded_statements_on_same_line_experimental)
- [91. csharp_new_line_before_catch](#91-csharp_new_line_before_catch)
- [92. csharp_new_line_before_else](#92-csharp_new_line_before_else)
- [93. csharp_new_line_before_finally](#93-csharp_new_line_before_finally)
- [94. csharp_new_line_before_members_in_anonymous_types](#94-csharp_new_line_before_members_in_anonymous_types)
- [95. csharp_new_line_before_members_in_object_initializers](#95-csharp_new_line_before_members_in_object_initializers)
- [96. csharp_new_line_before_open_brace](#96-csharp_new_line_before_open_brace)
- [97. csharp_new_line_between_query_expression_clauses](#97-csharp_new_line_between_query_expression_clauses)
- [98. csharp_indent_block_contents](#98-csharp_indent_block_contents)
- [99. csharp_indent_braces](#99-csharp_indent_braces)
- [100. csharp_indent_case_contents](#100-csharp_indent_case_contents)
- [101. csharp_indent_case_contents_when_block](#101-csharp_indent_case_contents_when_block)
- [102. csharp_indent_labels](#102-csharp_indent_labels)
- [103. csharp_indent_switch_labels](#103-csharp_indent_switch_labels)
- [104. csharp_space_after_cast](#104-csharp_space_after_cast)
- [105. csharp_space_after_colon_in_inheritance_clause](#105-csharp_space_after_colon_in_inheritance_clause)
- [106. csharp_space_after_comma](#106-csharp_space_after_comma)
- [107. csharp_space_after_dot](#107-csharp_space_after_dot)
- [108. csharp_space_after_keywords_in_control_flow_statements](#108-csharp_space_after_keywords_in_control_flow_statements)
- [109. csharp_space_after_semicolon_in_for_statement](#109-csharp_space_after_semicolon_in_for_statement)
- [110. csharp_space_around_binary_operators](#110-csharp_space_around_binary_operators)
- [111. csharp_space_around_declaration_statements](#111-csharp_space_around_declaration_statements)
- [112. csharp_space_before_colon_in_inheritance_clause](#112-csharp_space_before_colon_in_inheritance_clause)
- [113. csharp_space_before_comma](#113-csharp_space_before_comma)
- [114. csharp_space_before_dot](#114-csharp_space_before_dot)
- [115. csharp_space_before_open_square_brackets](#115-csharp_space_before_open_square_brackets)
- [116. csharp_space_before_semicolon_in_for_statement](#116-csharp_space_before_semicolon_in_for_statement)
- [117. csharp_space_between_empty_square_brackets](#117-csharp_space_between_empty_square_brackets)
- [118. csharp_space_between_method_call_empty_parameter_list_parentheses](#118-csharp_space_between_method_call_empty_parameter_list_parentheses)
- [119. csharp_space_between_method_call_name_and_opening_parenthesis](#119-csharp_space_between_method_call_name_and_opening_parenthesis)
- [120. csharp_space_between_method_call_parameter_list_parentheses](#120-csharp_space_between_method_call_parameter_list_parentheses)
- [121. csharp_space_between_method_declaration_empty_parameter_list_parentheses](#121-csharp_space_between_method_declaration_empty_parameter_list_parentheses)
- [122. csharp_space_between_method_declaration_name_and_open_parenthesis](#122-csharp_space_between_method_declaration_name_and_open_parenthesis)
- [123. csharp_space_between_method_declaration_parameter_list_parentheses](#123-csharp_space_between_method_declaration_parameter_list_parentheses)
- [124. csharp_space_between_parentheses](#124-csharp_space_between_parentheses)
- [125. csharp_space_between_square_brackets](#125-csharp_space_between_square_brackets)
- [126. csharp_preserve_single_line_blocks](#126-csharp_preserve_single_line_blocks)
- [127. csharp_preserve_single_line_statements](#127-csharp_preserve_single_line_statements)
- [128. dotnet_naming_rule.interface_should_be_begins_with_i](#128-dotnet_naming_ruleinterface_should_be_begins_with_i)
- [129. dotnet_naming_rule.types_should_be_pascal_case](#129-dotnet_naming_ruletypes_should_be_pascal_case)
- [130. dotnet_naming_rule.non_field_members_should_be_pascal_case](#130-dotnet_naming_rulenon_field_members_should_be_pascal_case)
- [131. trim_trailing_whitespace](#131-trim_trailing_whitespace)
- [132. dotnet_diagnostic.IDE0005.severity](#132-dotnet_diagnosticide0005severity)
- [133. dotnet_diagnostic.IDE1006.severity](#133-dotnet_diagnosticide1006severity)
- [134. dotnet_diagnostic.CS8019.severity](#134-dotnet_diagnosticcs8019severity)
- [135. dotnet_diagnostic.IDE0079.severity](#135-dotnet_diagnosticide0079severity)
- [136. dotnet_diagnostic.IDE0130.severity](#136-dotnet_diagnosticide0130severity)
- [137. dotnet_diagnostic.CS1591.severity](#137-dotnet_diagnosticcs1591severity)
- [138. csharp_prefer_system_threading_lock](#138-csharp_prefer_system_threading_lock)

</details>

---
# `Rules`

## 1. indent_size  
**Description**: Defines the number of spaces used for each indentation level.  

---
## 2. indent_style  
**Description**: Defines whether to use spaces or tabs for indentation.  

---
## 3. tab_width  
**Description**: Sets the number of columns used to represent a tab character if `indent_style=tab`.  

---
## 4. end_of_line  
**Description**: Sets the line ending character(s) to use (e.g., `crlf` for Windows).  

---
## 5. insert_final_newline  
**Description**: Specifies whether to ensure the file ends with a newline.  

---
## 6. dotnet_separate_import_directive_groups  
**Description**: Controls whether using directives are separated into groups by blank lines.  

---
## 7. dotnet_sort_system_directives_first  
**Description**: Enforces whether 'System' namespaces come first in usings.  

---
## 8. file_header_template  
**Description**: Controls the file header text inserted in new files.  

---
## 9. dotnet_style_qualification_for_event  
**Description**: Enforces use of `this.` qualifier for events.  
\
**Examples**  
When True  
```csharp  
this.eventHandler?.Invoke(this, EventArgs.Empty);  
```  
When False  
```csharp  
eventHandler?.Invoke(this, EventArgs.Empty);  
```  

---
## 10. dotnet_style_qualification_for_field  
**Description**: Enforces use of `this.` qualifier for fields.  
\
**Examples**  
When True  
```csharp  
this.myField = 10;  
```  
When False  
```csharp  
myField = 10;  
```  

---
## 11. dotnet_style_qualification_for_method  
**Description**: Enforces use of `this.` qualifier for methods.  
\
**Examples**  
When True  
```csharp  
this.DoSomething();  
```  
When False  
```csharp  
DoSomething();  
```  

---
## 12. dotnet_style_qualification_for_property  
**Description**: Enforces use of `this.` qualifier for properties.  
\
**Examples**  
When True  
```csharp  
this.MyProperty = 5;  
```  
When False  
```csharp  
MyProperty = 5;  
```  

---
## 13. dotnet_style_predefined_type_for_locals_parameters_members  
**Description**: Prefers language keywords (e.g., `int`) over BCL types (e.g., `Int32`).  
\
**Examples**  
When True  
```csharp  
int x = 0;  
```  
When False  
```csharp  
Int32 x = 0;  
```  

---
## 14. dotnet_style_predefined_type_for_member_access  
**Description**: Prefers language keywords when accessing static members.  
\
**Examples**  
When True  
```csharp  
string.Empty;  
```  
When False  
```csharp  
String.Empty;  
```  

---
## 15. dotnet_style_parentheses_in_arithmetic_binary_operators  
**Description**: Enforces parentheses around arithmetic expressions for clarity.  
\
**Examples**  
Option 1  
```csharp  
(a + b) * c;  
```  
Option 2  
```csharp  
a + b * c;  
```  

---
## 16. dotnet_style_parentheses_in_other_binary_operators  
**Description**: Enforces parentheses for non-arithmetic binary operators.  
\
**Examples**  
Option 1  
```csharp  
(x & y) == 0;  
```  
Option 2  
```csharp  
x & y == 0;  
```  

---
## 17. dotnet_style_parentheses_in_other_operators  
**Description**: Controls parentheses usage for cast/unary operators.  
\
**Examples**  
Option 1  
```csharp  
(int)x + 1;  
```  
Option 2  
```csharp  
(int)x + (1);  
```  

---
## 18. dotnet_style_parentheses_in_relational_binary_operators  
**Description**: Enforces parentheses around relational operators.  
\
**Examples**  
Option 1  
```csharp  
(a < b) == true;  
```  
Option 2  
```csharp  
a < b == true;  
```  

---
## 19. dotnet_style_require_accessibility_modifiers  
**Description**: Enforces accessibility keywords on members.  
\
**Examples**  
When True  
```csharp  
public void MyMethod() { }  
```  
When False  
```csharp  
void MyMethod() { }  
```  

---
## 20. dotnet_style_coalesce_expression  
**Description**: Prefers `??` operator over conditional expressions for null checks.  
\
**Examples**  
When True  
```csharp  
var result = value ?? "default";  
```  
When False  
```csharp  
var result = value != null ? value : "default";  
```  

---
## 21. dotnet_style_collection_initializer  
**Description**: Enforces using collection initializers.  
\
**Examples**  
When True  
```csharp  
var list = new List<int> { 1, 2, 3 };  
```  
When False  
```csharp  
var list = new List<int>();  
list.Add(1);  
list.Add(2);  
list.Add(3);  
```  

---
## 22. dotnet_style_explicit_tuple_names  
**Description**: Ensures tuple elements have explicit names.  
\
**Examples**  
When True  
```csharp  
(int Id, string Name) person = (1, "John");  
```  
When False  
```csharp  
(int, string) person = (1, "John");  
```  

---
## 23. dotnet_style_namespace_match_folder  
**Description**: Enforces that namespaces match the folder structure.  
\
**Examples**  
When True  
```csharp  
// File: MyProject/Utilities/Logger.cs  
namespace MyProject.Utilities;  
```  
When False  
```csharp  
// File: MyProject/Utilities/Logger.cs  
namespace SomeRandomName;  
```  

---
## 24. dotnet_style_null_propagation  
**Description**: Prefers `?.` operator over explicit null checks.  
\
**Examples**  
When True  
```csharp  
var length = str?.Length;  
```  
When False  
```csharp  
var length = str == null ? 0 : str.Length;  
```  

---
## 25. dotnet_style_object_initializer  
**Description**: Enforces using object initializers.  
\
**Examples**  
When True  
```csharp  
var person = new Person { Name = "Alice", Age = 30 };  
```  
When False  
```csharp  
var person = new Person();  
person.Name = "Alice";  
person.Age = 30;  
```  

---
## 26. dotnet_style_operator_placement_when_wrapping  
**Description**: Sets operator placement when wrapping lines.  
\
**Examples**  
Option 1 (beginning_of_line):  
```csharp  
var sum = a  
    + b  
    + c;  
```  
Option 2 (end_of_line):  
```csharp  
var sum = a +  
    b +  
    c;  
```  

---
## 27. dotnet_style_prefer_auto_properties  
**Description**: Prefers auto-properties over explicit backing fields.  
\
**Examples**  
When True  
```csharp  
public int Age { get; set; }  
```  
When False  
```csharp  
private int _age;  
public int Age { get => _age; set => _age = value; }  
```  

---
## 28. dotnet_style_prefer_collection_expression  
**Description**: Prefers collection expressions (e.g., `[1, 2, 3]`).  
\
**Examples**  
Option 1  
```csharp  
var list = [1, 2, 3];  
```  
Option 2  
```csharp  
var list = new List<int> { 1, 2, 3 };  
```  

---
## 29. dotnet_style_prefer_compound_assignment  
**Description**: Prefers compound assignment operators (e.g., `+=`).  
\
**Examples**  
When True  
```csharp  
x += 1;  
```  
When False  
```csharp  
x = x + 1;  
```  

---
## 30. dotnet_style_prefer_conditional_expression_over_assignment  
**Description**: Prefers conditional expressions over `if` statements for assignments.  
\
**Examples**  
When True  
```csharp  
var result = condition ? "Yes" : "No";  
```  
When False  
```csharp  
string result;  
if (condition) result = "Yes";  
else result = "No";  
```  

---
## 31. dotnet_style_prefer_conditional_expression_over_return  
**Description**: Prefers conditional expressions over `if` statements for returns.  
\
**Examples**  
When True  
```csharp  
return condition ? "Yes" : "No";  
```  
When False  
```csharp  
if (condition) return "Yes";  
return "No";  
```  

---
## 32. dotnet_style_prefer_foreach_explicit_cast_in_source  
**Description**: Prefers explicit casting in `foreach` loops when types are known.  
\
**Examples**  
Option 1  
```csharp  
foreach (string x in collectionOfObjects) { }  
```  
Option 2  
```csharp  
foreach (var x in collectionOfObjects.Cast<string>()) { }  
```  

---
## 33. dotnet_style_prefer_inferred_anonymous_type_member_names  
**Description**: Omits redundant property names in anonymous types.  
\
**Examples**  
When True  
```csharp  
var anon = new { FirstName, LastName };  
```  
When False  
```csharp  
var anon = new { FirstName = FirstName, LastName = LastName };  
```  

---
## 34. dotnet_style_prefer_inferred_tuple_names  
**Description**: Omits redundant tuple element names.  
\
**Examples**  
When True  
```csharp  
var person = (firstName, lastName);  
```  
When False  
```csharp  
var person = (firstName: firstName, lastName: lastName);  
```  

---
## 35. dotnet_style_prefer_is_null_check_over_reference_equality_method  
**Description**: Prefers `is null` over `ReferenceEquals(obj, null)`.  
\
**Examples**  
When True  
```csharp  
if (obj is null) { }  
```  
When False  
```csharp  
if (ReferenceEquals(obj, null)) { }  
```  

---
## 36. dotnet_style_prefer_simplified_boolean_expressions  
**Description**: Prefers simplified boolean expressions.  
\
**Examples**  
When True  
```csharp  
if (flag) { }  
```  
When False  
```csharp  
if (flag == true) { }  
```  

---
## 37. dotnet_style_prefer_simplified_interpolation  
**Description**: Prefers simplified string interpolation.  
\
**Examples**  
When True  
```csharp  
$"Hello {name}";  
```  
When False  
```csharp  
$"Hello {name.ToString()}";  
```  

---
## 38. dotnet_style_readonly_field  
**Description**: Enforces `readonly` for immutable fields.  
\
**Examples**  
When True  
```csharp  
private readonly int _count = 0;  
```  
When False  
```csharp  
private int _count = 0;  
```  

---
## 39. dotnet_code_quality_unused_parameters  
**Description**: Configures how unused parameters are handled.  
\
**Examples**  
Option 1 (align with interface):  
```csharp  
void IInterface.Method(int unused) { }  
```  
Option 2 (warning):  
```csharp  
void Method(int unused) { } // Warning  
```  

---
## 40. dotnet_remove_unnecessary_suppression_exclusions  
**Description**: Controls which suppressions are considered unnecessary.  

---
## 41. dotnet_style_allow_multiple_blank_lines_experimental  
**Description**: Controls whether multiple consecutive blank lines are allowed.  

---
## 42. dotnet_style_allow_statement_immediately_after_block_experimental  
**Description**: Controls whether statements can follow closing braces on the same line.  
\
**Examples**  
When True  
```csharp  
if (condition)  
{  
    DoSomething();  
} DoSomethingElse();  
```  
When False  
```csharp  
if (condition)  
{  
    DoSomething();  
}  
DoSomethingElse();  
```  

---
## 43. csharp_style_var_elsewhere  
**Description**: Controls `var` usage for non-built-in types.  
\
**Examples**  
When True  
```csharp  
int x = 0;  
```  
When False  
```csharp  
var x = 0;  
```  

---
## 44. csharp_style_var_for_built_in_types  
**Description**: Enforces `var` for built-in types.  
\
**Examples**  
When True  
```csharp  
var x = 0;  
```  
When False  
```csharp  
int x = 0;  
```  

---
## 45. csharp_style_var_when_type_is_apparent  
**Description**: Enforces `var` when the type is obvious.  
\
**Examples**  
When True  
```csharp  
var stream = new MemoryStream();  
```  
When False  
```csharp  
MemoryStream stream = new MemoryStream();  
```  

---
## 46. csharp_style_expression_bodied_accessors  
**Description**: Enforces expression-bodied syntax for property accessors.  
\
**Examples**  
When True  
```csharp  
public int Age => _age;  
```  
When False  
```csharp  
public int Age { get { return _age; } }  
```  

---
## 47. csharp_style_expression_bodied_constructors  
**Description**: Enforces expression-bodied syntax for constructors.  
\
**Examples**  
When True  
```csharp  
public Person() => Name = "Unknown";  
```  
When False  
```csharp  
public Person()  
{  
    Name = "Unknown";  
}  
```  

---
## 48. csharp_style_expression_bodied_indexers  
**Description**: Enforces expression-bodied syntax for indexers.  
\
**Examples**  
When True  
```csharp  
public int this[int index] => _items[index];  
```  
When False  
```csharp  
public int this[int index]  
{  
    get { return _items[index]; }  
}  
```  

---
## 49. csharp_style_expression_bodied_lambdas  
**Description**: Enforces expression-bodied syntax for lambdas.  
\
**Examples**  
When True  
```csharp  
var func = x => x * 2;  
```  
When False  
```csharp  
var func = x =>  
{  
    return x * 2;  
};  
```  

---
## 50. csharp_style_expression_bodied_local_functions  
**Description**: Enforces expression-bodied syntax for local functions.  
\
**Examples**  
When True  
```csharp  
int Sum(int a, int b) => a + b;  
```  
When False  
```csharp  
int Sum(int a, int b)  
{  
    return a + b;  
}  
```  

---
## 51. csharp_style_expression_bodied_methods  
**Description**: Enforces expression-bodied syntax for methods.  
\
**Examples**  
When True  
```csharp  
public int GetValue() => 42;  
```  
When False  
```csharp  
public int GetValue()  
{  
    return 42;  
}  
```  

---
## 52. csharp_style_expression_bodied_operators  
**Description**: Enforces expression-bodied syntax for operator overloads.  
\
**Examples**  
When True  
```csharp  
public static Vector operator +(Vector a, Vector b) => new(a.X + b.X, a.Y + b.Y);  
```  
When False  
```csharp  
public static Vector operator +(Vector a, Vector b)  
{  
    return new Vector(a.X + b.X, a.Y + b.Y);  
}  
```  

---
## 53. csharp_style_expression_bodied_properties  
**Description**: Enforces expression-bodied syntax for properties.  
\
**Examples**  
When True  
```csharp  
public int MyProperty => _myField;  
```  
When False  
```csharp  
public int MyProperty  
{  
    get { return _myField; }  
}  
```  

---
## 54. csharp_style_pattern_matching_over_as_with_null_check  
**Description**: Prefers pattern matching over `as` + null check.  
\
**Examples**  
When True  
```csharp  
if (obj is MyClass c) { }  
```  
When False  
```csharp  
var c = obj as MyClass;  
if (c != null) { }  
```  

---
## 55. csharp_style_pattern_matching_over_is_with_cast_check  
**Description**: Prefers pattern matching over `is` + cast.  
\
**Examples**  
When True  
```csharp  
if (obj is MyClass c) { /* ... */ }  
```  
When False  
```csharp  
if (obj is MyClass) { var c = (MyClass)obj; /* ... */ }  
```  

---
## 56. csharp_style_prefer_extended_property_pattern  
**Description**: Prefers extended property patterns (e.g., `{ Property: 10 }`).  
\
**Examples**  
When True  
```csharp  
if (obj is { Property: 10 }) { /* ... */ }  
```  
When False  
```csharp  
if (obj is MyClass { Property: 10 }) { /* ... */ }  
```  

---
## 57. csharp_style_prefer_not_pattern  
**Description**: Prefers `not` pattern over `!` operator for negation.  
\
**Examples**  
When True  
```csharp  
if (obj is not null) { /* ... */ }  
```  
When False  
```csharp  
if (!(obj is null)) { /* ... */ }  
```  

---
## 58. csharp_style_prefer_pattern_matching  
**Description**: Prefers pattern matching expressions overall when possible.  
\
**Examples**  
When True  
```csharp  
if (obj is MyClass c) { /* ... */ }  
```  
When False  
```csharp  
if (obj is MyClass) { var c = (MyClass)obj; /* ... */ }  
```  

---
## 59. csharp_style_prefer_switch_expression  
**Description**: Prefers switch expressions over switch statements.  
\
**Examples**  
When True  
```csharp  
return input switch { 1 => "one", 2 => "two", _ => "other" };  
```  
When False  
```csharp  
switch (input)  
{  
    case 1: return "one";  
    case 2: return "two";  
    default: return "other";  
}  
```  

---
## 60. csharp_style_conditional_delegate_call  
**Description**: Prefers `?.Invoke()` syntax over explicit null checks for delegates.  
\
**Examples**  
When True  
```csharp  
MyEvent?.Invoke(this, EventArgs.Empty);  
```  
When False  
```csharp  
if (MyEvent != null) { MyEvent(this, EventArgs.Empty); }  
```  

---
## 61. csharp_prefer_static_anonymous_function  
**Description**: Prefers `static` anonymous functions when they don’t capture outer variables.  
\
**Examples**  
When True  
```csharp  
Func<int, int> sq = static x => x * x;  
```  
When False  
```csharp  
Func<int, int> sq = x => x * x;  
```  

---
## 62. csharp_prefer_static_local_function  
**Description**: Prefers `static` local functions when they don’t capture outer variables.  
\
**Examples**  
When True  
```csharp  
static int Add(int a, int b) => a + b;  
```  
When False  
```csharp  
int Add(int a, int b) => a + b;  
```  

---
## 63. csharp_preferred_modifier_order  
**Description**: Enforces the order of modifiers (e.g., `public static` over `static public`).  
\
**Examples**  
Correct Order  
```csharp  
public static int MyValue;  
```  
Incorrect Order  
```csharp  
static public int MyValue;  
```  

---
## 64. csharp_style_prefer_readonly_struct  
**Description**: Enforces `readonly struct` for immutable structs.  
\
**Examples**  
When True  
```csharp  
public readonly struct MyStruct { /* ... */ }  
```  
When False  
```csharp  
public struct MyStruct { /* ... */ }  
```  

---
## 65. csharp_style_prefer_readonly_struct_member  
**Description**: Enforces `readonly` on struct members where possible.  
\
**Examples**  
When True  
```csharp  
public readonly int GetValue() => _value;  
```  
When False  
```csharp  
public int GetValue() => _value;  
```  

---
## 66. csharp_prefer_braces  
**Description**: Enforces braces for control flow statements.  
\
**Examples**  
When True  
```csharp  
if (condition)  
{  
    DoSomething();  
}  
```  
When False  
```csharp  
if (condition) DoSomething();  
```  

---
## 67. csharp_prefer_simple_using_statement  
**Description**: Enforces simplified `using` statements (C# 8+).  
\
**Examples**  
When True  
```csharp  
using var file = new FileStream(...);  
```  
When False  
```csharp  
using (var file = new FileStream(...)) { /* ... */ }  
```  

---
## 68. csharp_style_namespace_declarations  
**Description**: Enforces file-scoped or block-scoped namespace declarations.  
\
**Examples**  
File-Scoped  
```csharp  
namespace MyNamespace;  
```  
Block-Scoped  
```csharp  
namespace MyNamespace  
{  
    // ...  
}  
```  

---
## 69. csharp_style_prefer_method_group_conversion  
**Description**: Prefers method groups over lambda expressions when equivalent.  
\
**Examples**  
When True  
```csharp  
list.ForEach(Console.WriteLine);  
```  
When False  
```csharp  
list.ForEach(x => Console.WriteLine(x));  
```  

---
## 70. csharp_style_prefer_primary_constructors  
**Description**: Prefers primary constructors for classes.  
\
**Examples**  
When True  
```csharp  
public class Person(string name) { /* ... */ }  
```  
When False  
```csharp  
public class Person  
{  
    public Person(string name) { /* ... */ }  
}  
```  

---
## 71. csharp_style_prefer_top_level_statements  
**Description**: Prefers top-level statements over explicit `Program` class.  
\
**Examples**  
When True  
```csharp  
Console.WriteLine("Hello, World!");  
```  
When False  
```csharp  
class Program  
{  
    static void Main()  
    {  
        Console.WriteLine("Hello, World!");  
    }  
}  
```  

---
## 72. csharp_prefer_simple_default_expression  
**Description**: Prefers `default` over `default(T)`.  
\
**Examples**  
When True  
```csharp  
var value = default;  
```  
When False  
```csharp  
var value = default(int);  
```  

---
## 73. csharp_style_deconstructed_variable_declaration  
**Description**: Prefers `var (x, y)` syntax for deconstruction.  
\
**Examples**  
When True  
```csharp  
var (x, y) = GetValues();  
```  
When False  
```csharp  
(int x, int y) = GetValues();  
```  

---
## 74. csharp_style_implicit_object_creation_when_type_is_apparent  
**Description**: Prefers `new()` over explicit type when apparent.  
\
**Examples**  
When True  
```csharp  
List<int> numbers = new();  
```  
When False  
```csharp  
List<int> numbers = new List<int>();  
```  

---
## 75. csharp_style_inlined_variable_declaration  
**Description**: Prefers inline variable declarations (e.g., `out int x`).  
\
**Examples**  
When True  
```csharp  
if (int.TryParse(str, out int x)) { /* ... */ }  
```  
When False  
```csharp  
int x;  
if (int.TryParse(str, out x)) { /* ... */ }  
```  

---
## 76. csharp_style_prefer_index_operator  
**Description**: Prefers `^` operator for end-based indexing.  
\
**Examples**  
When True  
```csharp  
var lastItem = array[^1];  
```  
When False  
```csharp  
var lastItem = array[array.Length - 1];  
```  

---
## 77. csharp_style_prefer_local_over_anonymous_function  
**Description**: Prefers local functions over anonymous lambdas.  
\
**Examples**  
When True  
```csharp  
int Sum(int a, int b) => a + b;  
```  
When False  
```csharp  
Func<int, int, int> sum = (a, b) => a + b;  
```  

---
## 78. csharp_style_prefer_null_check_over_type_check  
**Description**: Prefers null checks over type checks (e.g., `obj is null`).  
\
**Examples**  
When True  
```csharp  
if (obj is null) { /* ... */ }  
```  
When False  
```csharp  
if (!(obj is SomeType)) { /* ... */ }  
```  

---
## 79. csharp_style_prefer_range_operator  
**Description**: Prefers `..` operator for slicing.  
\
**Examples**  
When True  
```csharp  
var slice = array[1..3];  
```  
When False  
```csharp  
var slice = array.Skip(1).Take(2);  
```  

---
## 80. csharp_style_prefer_tuple_swap  
**Description**: Prefers tuple swap syntax (e.g., `(x, y) = (y, x)`).  
\
**Examples**  
When True  
```csharp  
(x, y) = (y, x);  
```  
When False  
```csharp  
var temp = x;  
x = y;  
y = temp;  
```  

---
## 81. csharp_style_prefer_utf8_string_literals  
**Description**: Prefers `u8` suffix for UTF-8 string literals.  
\
**Examples**  
When True  
```csharp  
var bytes = "Hello"u8;  
```  
When False  
```csharp  
var bytes = Encoding.UTF8.GetBytes("Hello");  
```  

---
## 82. csharp_style_throw_expression  
**Description**: Prefers `throw` expressions over separate `if` checks.  
\
**Examples**  
When True  
```csharp  
var person = value ?? throw new ArgumentNullException(nameof(value));  
```  
When False  
```csharp  
if (value == null) throw new ArgumentNullException(nameof(value));  
```  

---
## 83. csharp_style_unused_value_assignment_preference  
**Description**: Defines handling of unused assignments (e.g., `_ = ...`).  
\
**Examples**  
Option 1 (discard):  
```csharp  
_ = SomeMethod();  
```  
Option 2 (unused local):  
```csharp  
var unused = SomeMethod();  
```  

---
## 84. csharp_style_unused_value_expression_statement_preference  
**Description**: Defines handling of unused expression statements.  
\
**Examples**  
Option 1 (discard):  
```csharp  
_ = SomeMethod();  
```  
Option 2 (remove):  
```csharp  
SomeMethod();  
```  

---
## 85. csharp_using_directive_placement  
**Description**: Enforces placement of `using` directives (inside/outside namespace).  
\
**Examples**  
Outside Namespace  
```csharp  
using System;  
namespace MyNamespace;  
```  
Inside Namespace  
```csharp  
namespace MyNamespace  
{  
    using System;  
}  
```  

---
## 86. csharp_style_allow_blank_line_after_colon_in_constructor_initializer_experimental  
**Description**: Allows/disallows blank lines after `:` in constructor initializers.  
\
**Examples**  
When True  
```csharp  
public MyClass() :  
    base() { }  
```  
When False  
```csharp  
public MyClass() : base() { }  
```  

---
## 87. csharp_style_allow_blank_line_after_token_in_arrow_expression_clause_experimental  
**Description**: Allows/disallows blank lines after `=>` in expression-bodied members.  
\
**Examples**  
When True  
```csharp  
public int GetValue() =>  
    42;  
```  
When False  
```csharp  
public int GetValue() => 42;  
```  

---
## 88. csharp_style_allow_blank_line_after_token_in_conditional_expression_experimental  
**Description**: Allows/disallows blank lines after `?`/`:` in ternary expressions.  
\
**Examples**  
When True  
```csharp  
var result = condition ?  
    "Yes" :  
    "No";  
```  
When False  
```csharp  
var result = condition ? "Yes" : "No";  
```  

---
## 89. csharp_style_allow_blank_lines_between_consecutive_braces_experimental  
**Description**: Allows/disallows blank lines between consecutive braces.  
\
**Examples**  
When True  
```csharp  
{  
    {  
    }  
}  
```  
When False  
```csharp  
{  
    {  
    }  
}  
```  

---
## 90. csharp_style_allow_embedded_statements_on_same_line_experimental  
**Description**: Allows/disallows embedded statements on the same line.  
\
**Examples**  
When True  
```csharp  
if (x) { y++; }  
```  
When False  
```csharp  
if (x)  
{  
    y++;  
}  
```  

---
## 91. csharp_new_line_before_catch  
**Description**: Enforces new line before `catch`.  
\
**Examples**  
When True  
```csharp  
try  
{  
}  
catch  
{  
}  
```  
When False  
```csharp  
try { } catch { }  
```  

---
## 92. csharp_new_line_before_else  
**Description**: Enforces new line before `else`.  
\
**Examples**  
When True  
```csharp  
if (condition)  
{  
}  
else  
{  
}  
```  
When False  
```csharp  
if (condition) { } else { }  
```  

---
## 93. csharp_new_line_before_finally  
**Description**: Enforces new line before `finally`.  
\
**Examples**  
When True  
```csharp  
try  
{  
}  
finally  
{  
}  
```  
When False  
```csharp  
try { } finally { }  
```  

---
## 94. csharp_new_line_before_members_in_anonymous_types  
**Description**: Enforces new lines between members in anonymous types.  
\
**Examples**  
When True  
```csharp  
var anon = new  
{  
    Name = "Alice",  
    Age = 30  
};  
```  
When False  
```csharp  
var anon = new { Name = "Alice", Age = 30 };  
```  

---
## 95. csharp_new_line_before_members_in_object_initializers  
**Description**: Enforces new lines between members in object initializers.  
\
**Examples**  
When True  
```csharp  
var person = new Person  
{  
    Name = "Bob",  
    Age = 20  
};  
```  
When False  
```csharp  
var person = new Person { Name = "Bob", Age = 20 };  
```  

---
## 96. csharp_new_line_before_open_brace  
**Description**: Enforces new line before opening braces.  
\
**Examples**  
When True  
```csharp  
if (condition)  
{  
}  
```  
When False  
```csharp  
if (condition) {  
}  
```  

---
## 97. csharp_new_line_between_query_expression_clauses  
**Description**: Enforces new lines between query clauses.  
\
**Examples**  
When True  
```csharp  
var result = from x in collection  
             where x > 0  
             select x;  
```  
When False  
```csharp  
var result = from x in collection where x > 0 select x;  
```  

---
## 98. csharp_indent_block_contents  
**Description**: Enforces indentation of block contents.  
\
**Examples**  
When True  
```csharp  
{  
    statement;  
}  
```  
When False  
```csharp  
{  
statement;  
}  
```  

---
## 99. csharp_indent_braces  
**Description**: Controls whether braces are indented.  
\
**Examples**  
When True  
```csharp  
if (condition)  
    {  
        statement;  
    }  
```  
When False  
```csharp  
if (condition)  
{  
    statement;  
}  
```  

---
## 100. csharp_indent_case_contents  
**Description**: Enforces indentation of `case` contents in `switch`.  
\
**Examples**  
When True  
```csharp  
switch (value)  
{  
    case 1:  
        DoSomething();  
        break;  
}  
```  
When False  
```csharp  
switch (value)  
{  
case 1:  
    DoSomething();  
    break;  
}  
```  

---
## 101. csharp_indent_case_contents_when_block  
**Description**: Enforces indentation of `case` blocks with braces.  
\
**Examples**  
When True  
```csharp  
case 1:  
{  
    DoSomething();  
    break;  
}  
```  
When False  
```csharp  
case 1:  
{  
DoSomething();  
break;  
}  
```  

---
## 102. csharp_indent_labels  
**Description**: Controls indentation level of labels.  
\
**Examples**  
Option 1 (one_less_than_current):  
```csharp  
    labelName:  
        DoSomething();  
```  
Option 2:  
```csharp  
labelName:  
    DoSomething();  
```  

---
## 103. csharp_indent_switch_labels  
**Description**: Enforces indentation of `switch` labels (`case`, `default`).  
\
**Examples**  
When True  
```csharp  
switch (value)  
{  
    case 1:  
        break;  
}  
```  
When False  
```csharp  
switch (value)  
{  
case 1:  
    break;  
}  
```  

---
## 104. csharp_space_after_cast  
**Description**: Controls spacing after cast operators.  
\
**Examples**  
When True  
```csharp  
(int) x;  
```  
When False  
```csharp  
(int)x;  
```  

---
## 105. csharp_space_after_colon_in_inheritance_clause  
**Description**: Controls spacing after `:` in base class/interface list.  
\
**Examples**  
When True  
```csharp  
class Derived : Base { }  
```  
When False  
```csharp  
class Derived :Base { }  
```  

---
## 106. csharp_space_after_comma  
**Description**: Controls spacing after commas.  
\
**Examples**  
When True  
```csharp  
var tuple = (1, 2);  
```  
When False  
```csharp  
var tuple = (1,2);  
```  

---
## 107. csharp_space_after_dot  
**Description**: Controls spacing after a dot.  
\
**Examples**  
When True  
```csharp  
obj. Property;  
```  
When False  
```csharp  
obj.Property;  
```  

---
## 108. csharp_space_after_keywords_in_control_flow_statements  
**Description**: Enforces spacing after keywords like `if`, `for`, `while`, etc.  
\
**Examples**  
When True  
```csharp  
if (condition) { }  
```  
When False  
```csharp  
if(condition) { }  
```  

---
## 109. csharp_space_after_semicolon_in_for_statement  
**Description**: Enforces spacing after semicolons in `for` statements.  
\
**Examples**  
When True  
```csharp  
for (int i = 0; i < 10; i++) { }  
```  
When False  
```csharp  
for (int i = 0;i < 10;i++) { }  
```  

---
## 110. csharp_space_around_binary_operators  
**Description**: Controls spacing around binary operators.  
\
**Examples**  
When True  
```csharp  
a + b;  
```  
When False  
```csharp  
a+b;  
```  

---
## 111. csharp_space_around_declaration_statements  
**Description**: Controls spacing around declaration statements.  
\
**Examples**  
When True  
```csharp  
int  x   =  0;  
```  
When False  
```csharp  
int x = 0;  
```  

---
## 112. csharp_space_before_colon_in_inheritance_clause  
**Description**: Controls spacing before `:` in base class/interface list.  
\
**Examples**  
When True  
```csharp  
class Derived : Base { }  
```  
When False  
```csharp  
class Derived: Base { }  
```  

---
## 113. csharp_space_before_comma  
**Description**: Controls spacing before commas.  
\
**Examples**  
When True  
```csharp  
var tuple = (1 , 2);  
```  
When False  
```csharp  
var tuple = (1, 2);  
```  

---
## 114. csharp_space_before_dot  
**Description**: Controls spacing before a dot.  
\
**Examples**  
When True  
```csharp  
obj .Property;  
```  
When False  
```csharp  
obj.Property;  
```  

---
## 115. csharp_space_before_open_square_brackets  
**Description**: Controls spacing before `[` in attributes or indexers.  
\
**Examples**  
When True  
```csharp  
[ Obsolete]  
```  
When False  
```csharp  
[Obsolete]  
```  

---
## 116. csharp_space_before_semicolon_in_for_statement  
**Description**: Controls spacing before semicolons in `for` statements.  
\
**Examples**  
When True  
```csharp  
for (int i = 0 ; i < 10 ; i++) { }  
```  
When False  
```csharp  
for (int i = 0; i < 10; i++) { }  
```  

---
## 117. csharp_space_between_empty_square_brackets  
**Description**: Controls spacing between empty brackets `[]`.  
\
**Examples**  
When True  
```csharp  
new int[ 0 ];  
```  
When False  
```csharp  
new int[0];  
```  

---
## 118. csharp_space_between_method_call_empty_parameter_list_parentheses  
**Description**: Controls spacing in empty parameter lists.  
\
**Examples**  
When True  
```csharp  
Method( );  
```  
When False  
```csharp  
Method();  
```  

---
## 119. csharp_space_between_method_call_name_and_opening_parenthesis  
**Description**: Controls spacing between method name and `(`.  
\
**Examples**  
When True  
```csharp  
Method (arg);  
```  
When False  
```csharp  
Method(arg);  
```  

---
## 120. csharp_space_between_method_call_parameter_list_parentheses  
**Description**: Controls spacing within parameter parentheses.  
\
**Examples**  
When True  
```csharp  
Method(a, b);  
```  
When False  
```csharp  
Method(a,b);  
```  

---
## 121. csharp_space_between_method_declaration_empty_parameter_list_parentheses  
**Description**: Controls spacing in empty parameter lists for methods.  
\
**Examples**  
When True  
```csharp  
void Method( );  
```  
When False  
```csharp  
void Method();  
```  

---
## 122. csharp_space_between_method_declaration_name_and_open_parenthesis  
**Description**: Controls spacing between method name and `(`.  
\
**Examples**  
When True  
```csharp  
void Method (string x);  
```  
When False  
```csharp  
void Method(string x);  
```  

---
## 123. csharp_space_between_method_declaration_parameter_list_parentheses  
**Description**: Controls spacing within method parameter parentheses.  
\
**Examples**  
When True  
```csharp  
void Method(int x, int y);  
```  
When False  
```csharp  
void Method(int x,int y);  
```  

---
## 124. csharp_space_between_parentheses  
**Description**: Controls spacing inside parentheses in expressions.  
\
**Examples**  
When True  
```csharp  
( x + y );  
```  
When False  
```csharp  
(x + y);  
```  

---
## 125. csharp_space_between_square_brackets  
**Description**: Controls spacing inside square brackets.  
\
**Examples**  
When True  
```csharp  
array[ 0 ];  
```  
When False  
```csharp  
array[0];  
```  

---
## 126. csharp_preserve_single_line_blocks  
**Description**: Controls whether single-line blocks are kept on one line.  
\
**Examples**  
When True  
```csharp  
if (condition) { DoSomething(); }  
```  
When False  
```csharp  
if (condition)  
{  
    DoSomething();  
}  
```  

---
## 127. csharp_preserve_single_line_statements  
**Description**: Controls whether single-line statements remain on one line.  
\
**Examples**  
When True  
```csharp  
if (condition) DoSomething();  
```  
When False  
```csharp  
if (condition)  
{  
    DoSomething();  
}  
```  

---
## 128. dotnet_naming_rule.interface_should_be_begins_with_i  
**Description**: Enforces interface names to start with `I`.  
\
**Examples**  
When True  
```csharp  
public interface IMyInterface { }  
```  
When False  
```csharp  
public interface MyInterface { }  
```  

---
## 129. dotnet_naming_rule.types_should_be_pascal_case  
**Description**: Enforces PascalCase for types (class, struct, enum, interface).  
\
**Examples**  
When True  
```csharp  
public class MyClass { }  
```  
When False  
```csharp  
public class myClass { }  
```  

---
## 130. dotnet_naming_rule.non_field_members_should_be_pascal_case  
**Description**: Enforces PascalCase for non-field members (properties, events, methods).  
\
**Examples**  
When True  
```csharp  
public void MyMethod() { }  
```  
When False  
```csharp  
public void myMethod() { }  
```  

---
## 131. trim_trailing_whitespace  
**Description**: Enforces removing trailing whitespace at the end of lines.  
\
**Examples**  
When True  
```csharp  
"Line with no trailing spaces"  
```  
When False  
```csharp  
"Line with trailing spaces   "  
```  

---
## 132. dotnet_diagnostic.IDE0005.severity  
**Description**: Configures severity for unnecessary usings (Roslyn analyzers).  
\
**Examples**  
When True  
```csharp  
using System; // if actually needed  
```  
When False  
```csharp  
using System; // if not used  
```  

---
## 133. dotnet_diagnostic.IDE1006.severity  
**Description**: Configures severity for naming rule violations.  

---
## 134. dotnet_diagnostic.CS8019.severity  
**Description**: Configures severity for unnecessary usings (C# compiler).  

---
## 135. dotnet_diagnostic.IDE0079.severity  
**Description**: Configures severity for redundant suppression of diagnostics.  

---
## 136. dotnet_diagnostic.IDE0130.severity  
**Description**: Configures severity for inconsistent `nameof` usage.  

---
## 137. dotnet_diagnostic.CS1591.severity  
**Description**: Configures severity for missing XML comment warnings.  

---
## 138. csharp_prefer_system_threading_lock  
**Description**: Enforces using `lock` keyword over `Monitor.Enter`.  
\
**Examples**  
When True  
```csharp  
lock (locker) { /* ... */ }  
```  
When False  
```csharp  
Monitor.Enter(locker); // manually  
```  