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
ms.openlocfilehash: fc8854bb0b406048d999324a034ebc62b100496c7cf4b5838733e9addd50d42f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000704"
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

 

 





