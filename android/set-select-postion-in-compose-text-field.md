# Set cursor position in Compose Text Field
If you want to set cursor position of a `TextField` in Compose, you can use [TextFieldValue](https://developer.android.com/reference/kotlin/androidx/compose/ui/text/input/TextFieldValue).  

Remember to use the overload version of [TextField](https://developer.android.com/reference/kotlin/androidx/compose/material/package-summary#TextField(androidx.compose.ui.text.input.TextFieldValue,kotlin.Function1,androidx.compose.ui.Modifier,kotlin.Boolean,kotlin.Boolean,androidx.compose.ui.text.TextStyle,kotlin.Function0,kotlin.Function0,kotlin.Function0,kotlin.Function0,kotlin.Boolean,androidx.compose.ui.text.input.VisualTransformation,androidx.compose.foundation.text.KeyboardOptions,androidx.compose.foundation.text.KeyboardActions,kotlin.Boolean,kotlin.Int,kotlin.Int,androidx.compose.foundation.interaction.MutableInteractionSource,androidx.compose.ui.graphics.Shape,androidx.compose.material.TextFieldColors)) which accepts a `TextFieldValue` type.

Code sample:

```kotlin
import androidx.compose.ui.text.input.TextFieldValue

val textFieldValue = TextFieldValue(
    text = "A word", 
    //Set cursor position here
    selection = TextRange(start = 0, end = 4)
)

TextField(
    value=textFieldValue,
    onValueChange={
        //TODO
    }
)
```