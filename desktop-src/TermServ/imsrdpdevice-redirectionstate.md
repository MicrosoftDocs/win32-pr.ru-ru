---
title: Имсрдпдевице Редиректионстате, свойство
description: Указывает состояние перенаправления устройства.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректионстате
- Службы удаленных рабочих столов свойства Редиректионстате, интерфейс Имсрдпдевице
- Службы удаленных рабочих столов интерфейса Имсрдпдевице, свойство Редиректионстате
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0f6fb5781700daa8a65443d2713253e97f73bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490344"
---
# <a name="imsrdpdeviceredirectionstate-property"></a>Свойство Имсрдпдевице:: Редиректионстате

Указывает состояние перенаправления устройства.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a>Значение свойства

Присвойте этому параметру значение **Variant \_ false** , чтобы отключить перенаправление или **вариант \_ true** , чтобы включить перенаправление.

## <a name="error-codes"></a>Коды ошибок

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="requirements"></a>Требования



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

 

 





