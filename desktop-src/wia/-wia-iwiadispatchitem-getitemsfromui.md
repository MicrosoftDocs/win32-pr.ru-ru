---
description: Метод Жетитемсфромуи объекта Item отображает диалоговое окно, позволяющее пользователю выбирать изображения и звук для передачи с устройства.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item. Жетитемсфромуи, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a954dbefec9728d2d6f595144ba3991ab4f7b3a1ded77fdf7e3ca5407be70d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669716"
---
# <a name="itemgetitemsfromui-method"></a>Item. Жетитемсфромуи, метод

Метод **жетитемсфромуи** объекта [**Item**](-wia-item.md) отображает диалоговое окно, позволяющее пользователю выбирать изображения и звук для передачи с устройства.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **виафлаг**](-wia-wiaflag.md)**

<dt>



  (0)


</dt> <dd>

По умолчанию. \[в \] задает поведение диалогового окна. Допустимые значения для этого параметра совпадают с параметрами параметра *лфлагс* метода [**девицедлг**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) .

</dd> </dl> </dd> <dt>

*Намерение* \[ окне\]
</dt> <dd>

Тип: **виаинтент**

<dt>



  (0)


</dt> <dd>

По умолчанию. \[в \] указывает, какой тип данных должен представлять изображение. Список значений намерения образа см. в разделе [**константы намерения изображения**](-wia-imageintentconstants.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **ICollection**

Этот метод возвращает коллекцию объектов [**Item**](-wia-item.md) , представляющих элементы, выбранные пользователем. Если элементы не выбраны, коллекция будет пустой.

## <a name="remarks"></a>Remarks

для приложений Microsoft Visual Basic добавьте ссылку на "Windows получения образа библиотеки типов 1,01".

Этот метод применяется только к устройствам (корневым элементам). Метод возвращает коллекцию объектов [**Item**](-wia-item.md) , представляющих изображения или аудиоклипы, выбранные пользователем.

Если пользователь не выбрал ни одного элемента, метод возвращает пустую коллекцию.

## <a name="examples"></a>Примеры

В следующем примере показано использование метода **жетитемсфромуи** , позволяющего пользователю выбирать изображения из диалогового окна.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




