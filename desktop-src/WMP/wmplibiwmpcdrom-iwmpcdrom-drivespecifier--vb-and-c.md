---
title: Ивмпкдром ДривеспеЦифиер, свойство
description: Свойство ДривеспеЦифиер получает букву CD или DVD-дисковода.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- проигрыватель Windows Media свойства дривеспеЦифиер
- проигрыватель Windows Media свойства дривеспеЦифиер, интерфейс ивмпкдром
- проигрыватель Windows Media интерфейса ивмпкдром, свойство дривеспеЦифиер
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b555cba0ec694a19a01c040a0369aeb473c6811933d45892cbf3c69ef640b8b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031464"
---
# <a name="iwmpcdromdrivespecifier-property"></a>Ивмпкдром: свойство РивеспеЦифиер:d

Свойство **дривеспеЦифиер** получает букву CD или DVD-дисковода.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a>Значение свойства

**Строка System. String** , которая является буквой диска.

## <a name="remarks"></a>Remarks

Обычно дисководы DVD могут воспроизводить компакт-диски, но дисководы компакт-дисков не могут воспроизводить DVD-носители.

Это свойство возвращает букву диска для индекса диска, начинающегося с нуля, в диапазоне, полученном с помощью **ивмпкдромколлектион. Count**. Полученное значение имеет вид *x*:, где *X* представляет букву диска.

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере **дривеспеЦифиер** используется для создания строки, содержащей список доступных ДИСКОВОДОВ компакт-дисков и дисков DVD, и отображает эту строку в окне сообщения. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпкдром (VB и C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Ивмпкдромколлектион. Count (VB и C#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Медиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





