---
description: Извлекает Иконтекстлинк по указанному индексу.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'Метод Иконтекстлинкс:: Жетконтекстлинк (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 01cf3b971b8533f21185a9b6e65c3cfb25109e657e2c9e2a931253d86c51dbdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940314"
---
# <a name="icontextlinksgetcontextlink-method"></a>Метод Иконтекстлинкс:: Жетконтекстлинк

Извлекает [**иконтекстлинк**](icontextlink.md) по указанному индексу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улиндекс* \[ окне\]
</dt> <dd>

Отсчитываемый от нуля индекс объекта [**иконтекстлинк**](icontextlink.md) , который необходимо получить.

</dd> <dt>

*ппконтекстлинк* \[ заполняет\]
</dt> <dd>

Указатель на объект [**иконтекстлинк**](icontextlink.md) по указанному индексу.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстлинк* , когда больше не нужно использовать контекстную ссылку.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтекстлинкс**](icontextlinks.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

