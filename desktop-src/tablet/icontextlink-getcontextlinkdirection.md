---
description: Извлекает тип отношения, представляемого этим Иконтекстлинк.
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: 'Метод Иконтекстлинк:: Жетконтекстлинкдиректион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 96506836e89f4bb2f8b202373df09b5cc6ee1c7f6e9e01f3b68bb2bbe2c8b56a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057914"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a>Метод Иконтекстлинк:: Жетконтекстлинкдиректион

Извлекает тип отношения, представляемого этим [**иконтекстлинк**](icontextlink.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекстлинкдиректион* \[ заполняет\]
</dt> <dd>

Направление, которое представляет этот [**иконтекстлинк**](icontextlink.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтекстлинк**](icontextlink.md)
</dt> <dt>

[**контекстлинкдиректион**](contextlinkdirection.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




