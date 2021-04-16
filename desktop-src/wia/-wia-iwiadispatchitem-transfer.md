---
description: Метод Transfer объекта Item передает данные с устройства в файл. Этот метод применяется только к элементам типа устройства.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Перемещение, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692523"
---
# <a name="itemtransfer-method"></a>Item. Перемещение, метод

Метод **Transfer** объекта [**Item**](-wia-item.md) передает данные с устройства в файл. Этот метод применяется только к элементам типа устройства.

## <a name="syntax"></a>Синтаксис


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя файла* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Указывает имя файла, в который передаются данные.

</dd> <dt>

*Асинктрансфер* \[ окне\]
</dt> <dd>

Тип: **Variant \_ bool**

Логическое значение, указывающее, следует ли выполнять пересылку как асинхронный вызов.

<dt>



 (Вариант \_ ЛОГИЧЕСКОМ


</dt> <dd>

По умолчанию. Задайте для этого параметра значение **true** , если вызов должен быть асинхронным (см. **Примечания**).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод применяется только к элементам типа файлов. Метод проверяет, что элемент поддерживает этот метод, прежде чем он попытается выполнить пересылку данных.

Используйте "Clipboard" в качестве параметра *filename* для перемещения элемента в буфер обмена.

Задайте для параметра *асинктрансфер* значение **false** для передачи в любом приложении или сценарии, работающем в среде, завершающей процесс в конце скрипта, например сервер сценариев Windows (WSH). В противном случае скрипт может завершиться, а процесс завершится до завершения перемещения.

Метод **передачи** не имеет возвращаемого значения. После завершения перемещения этот метод отправляет событие [**онтрансферкомплете**](-wia--iwiaevents-ontransfercomplete.md) в скрипт или приложение.

## <a name="examples"></a>Примеры

В следующем примере демонстрируется использование метода **перемещения** для перемещения данных с устройства.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




