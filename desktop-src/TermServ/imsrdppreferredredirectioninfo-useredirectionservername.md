---
title: Имсрдппреферредредиректионинфо Усередиректионсервернаме, свойство
description: Возвращает или задает значение, указывающее, следует ли использовать имя сервера перенаправления.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Усередиректионсервернаме
- Службы удаленных рабочих столов свойства Усередиректионсервернаме, интерфейс Имсрдппреферредредиректионинфо
- Службы удаленных рабочих столов интерфейса Имсрдппреферредредиректионинфо, свойство Усередиректионсервернаме
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801720"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a>Свойство Имсрдппреферредредиректионинфо:: Усередиректионсервернаме

Возвращает или задает значение, указывающее, следует ли использовать имя сервера перенаправления.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a>Значение свойства

Указывает, следует ли использовать имя сервера перенаправления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                    |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ имсрдппреферредредиректионинфо определен как FDD029F9-9574-4DEF-8529-64B521CCCAA4<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдппреферредредиректионинфо**](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





