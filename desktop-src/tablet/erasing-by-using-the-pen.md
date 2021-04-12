---
description: Если вы решили реализовать стирание в приложении, отличном от, с помощью объекта InkOverlay, это можно сделать с помощью одного из следующих двух методов.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Стирание с помощью пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423789"
---
# <a name="erasing-by-using-the-pen"></a>Стирание с помощью пера

Если вы решили реализовать стирание в приложении, отличном от, с помощью объекта [**InkOverlay**](inkoverlay-class.md) , это можно сделать с помощью одного из следующих двух методов.

## <a name="using-the-tip-of-the-pen"></a>Использование кончика пера

Совет планшетного пера обычно используется для рукописного ввода и рисования. Однако TIP можно также использовать для стирания рукописного ввода. Для этого приложение должно иметь режим стирания, который пользователи могут использовать. В этом режиме используйте проверку нажатия для определения рукописных данных, на которые курсор перемещается. Можно установить режим стирания, чтобы удалить только рукописные данные, передаваемые курсором, или целые фрагменты, пересекающие путь курсора, в зависимости от особенностей проектирования и функциональности.

Пример использования режима стирания для стирания рукописного ввода см. в [примере стирания рукописного ввода](ink-erasing-sample.md).

## <a name="using-the-top-of-the-pen"></a>Использование верхней части пера

Чтобы реализовать стирание с помощью верхней части пера планшета, приложение должно искать изменения в курсоре. Чтобы найти инвертированный курсор, прослушайте событие [**курсоринранже**](inkoverlay-cursorinrange.md) , чтобы определить, находится ли курсор в контексте приложения. Если курсор находится в диапазоне, найдите [**Инвертированное**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) свойство в объекте [**курсора**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) . Если **Инвертированное** свойство имеет **значение true**, выполните проверку нажатия, чтобы определить, на какие рукописные данные перемещается курсор. Удалите рукописный ввод или штрихи, пересекающие путь курсора, в зависимости от особенностей проектирования и функциональности.

Пример использования верхней части пера для стирания рукописного ввода см. в [примере стирания рукописного ввода](ink-erasing-sample.md).

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a>Определение, включено ли стирание с помощью верхней части пера

Пользователи могут использовать верхушку пера, чтобы стереть рукописные данные в приложениях, предназначенных для планшетных ПК, если они допускают их конкретное оборудование. Доступ к этой функции осуществляется с помощью флажка в поле Группа кнопок пера на вкладке Параметры пера диалогового окна Панель управления планшета и настройки пера. Чтобы определить, включил ли пользователь стирание в начало пера, проверьте следующий подраздел реестра:

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

`EraseEnable`Запись этого подраздела имеет тип **reg \_ DWORD**. Значение этой записи равно 1 для параметра включено или 0 для параметра отключено. Другие значения зарезервированы для использования в будущем.

Если приложение позволяет использовать верхушку пера для стирания, следует проверить и кэшировать значение записи Ерасинабле в следующих случаях:

-   Запустится приложение.
-   Всякий раз, когда приложение получает фокус после потери фокуса.

Используйте это кэшированное значение, чтобы соответствующим образом изменить поведение приложения.

В следующем примере на языке C \# определяется `GetEraseEnabled` метод, который проверяет значение `EraseEnable` записи в `SysEventParameters` подразделе. `GetEraseEnabled`Метод возвращает значение **true** , если значение записи равно 1; возвращает значение **false** , если значение записи равно 0, или вызывает исключение [InvalidOperationException](/dotnet/api/system.invalidoperationexception) , если значение записи отлично от 1 или 0. `GetEraseEnabled`Метод возвращает ожидаемое значение **true** , если не указан подраздел или запись.


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
