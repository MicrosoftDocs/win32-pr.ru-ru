---
title: Имсрдпдевице FriendlyName, свойство
description: Извлекает отображаемое имя для устройства.
ms.assetid: ed27eacd-1d39-484c-8217-62ed608db050
ms.tgt_platform: multiple
keywords:
- Свойство FriendlyName службы удаленных рабочих столов
- Свойство FriendlyName службы удаленных рабочих столов, интерфейс Имсрдпдевице
- Службы удаленных рабочих столов интерфейса Имсрдпдевице, свойство FriendlyName
topic_type:
- apiref
api_name:
- IMsRdpDevice.FriendlyName
- IMsRdpDevice.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d2b9ec817cdfa2a384e2f601da82a7e182b458574a5bb4b29fe639d8e11216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334624"
---
# <a name="imsrdpdevicefriendlyname-property"></a>Свойство Имсрдпдевице:: FriendlyName

Извлекает отображаемое имя для устройства.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_FriendlyName(
  [out] BSTR *pFriendlyName
);
```



## <a name="property-value"></a>Значение свойства

Отображаемое имя.

## <a name="error-codes"></a>Коды ошибок

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпдевице определен как 60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпдевице**](imsrdpdevice.md)
</dt> </dl>

 

 





