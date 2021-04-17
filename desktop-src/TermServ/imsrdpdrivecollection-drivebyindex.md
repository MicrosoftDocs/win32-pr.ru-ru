---
title: Имсрдпдривеколлектион Дривебиндекс, свойство
description: Извлекает диск по указанному индексу.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дривебиндекс
- Службы удаленных рабочих столов свойства Дривебиндекс, интерфейс Имсрдпдривеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдривеколлектион, свойство Дривебиндекс
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2789656b328f9615787ff2cd50a1b69c712a8138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415857"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a>Имсрдпдривеколлектион: свойство Ривебиндекс:D

Извлекает диск по указанному индексу.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a>Значение свойства

Указатель интерфейса [**имсрдпдриве**](imsrdpdrive.md) .

## <a name="error-codes"></a>Коды ошибок

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ имсрдпдривеколлектион определен как 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпдривеколлектион**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





