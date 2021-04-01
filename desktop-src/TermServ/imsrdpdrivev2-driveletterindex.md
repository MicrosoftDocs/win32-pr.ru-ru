---
title: IMsRdpDriveV2 Дривелеттериндекс, свойство
description: Содержит индекс буквы диска.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дривелеттериндекс
- Службы удаленных рабочих столов свойства Дривелеттериндекс, интерфейс IMsRdpDriveV2
- Службы удаленных рабочих столов интерфейса IMsRdpDriveV2, свойство Дривелеттериндекс
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989409"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a>IMsRdpDriveV2: свойство Ривелеттериндекс:D

Содержит индекс буквы диска.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a>Значение свойства

Индекс буквы для диска. 0 = "A", 1 = "B" и т. д.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7 с пакетом обновления 1 (SP1)<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpDriveV2**](imsrdpdrivev2.md)
</dt> </dl>

 

 





