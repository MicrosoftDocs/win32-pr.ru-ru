---
description: Добавляет новый Иконтекстлинк в коллекцию ссылок контекста объекта Иконтекстноде.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'Метод Иконтекстноде:: Аддконтекстлинк (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650551"
---
# <a name="icontextnodeaddcontextlink-method"></a>Метод Иконтекстноде:: Аддконтекстлинк

Добавляет новый [**иконтекстлинк**](icontextlink.md) в коллекцию ссылок контекста объекта [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдестинатионноде* \[ окне\]
</dt> <dd>

Целевой [**иконтекстноде**](icontextnode.md) для нового [**иконтекстлинк**](icontextlink.md).

</dd> <dt>

*линкдиректион* \[ окне\]
</dt> <dd>

Направление создаваемого объекта [**иконтекстлинк**](icontextlink.md) .

</dd> <dt>

*ппконтекстлинктоадд* \[ заполняет\]
</dt> <dd>

Указатель на новый объект [**иконтекстлинк**](icontextlink.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстлинктоадд* , когда больше не нужно использовать контекстный узел.

 

Этот объект [**иконтекстноде**](icontextnode.md) является исходным узлом (см. [**Иконтекстлинк:: жетсаурценоде**](icontextlink-getsourcenode.md)) для нового объекта [**иконтекстлинк**](icontextlink.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**иконтекстлинк**](icontextlink.md)
</dt> <dt>

[**иконтекстлинкс**](icontextlinks.md)
</dt> <dt>

[**контекстлинкдиректион**](contextlinkdirection.md)
</dt> <dt>

[**Иконтекстноде::D Елетеконтекстлинк**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**Иконтекстноде:: Жетконтекстлинкс**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

