---
description: Извлекает объект Иконтекстноде, который является назначением для этого Иконтекстлинк.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'Метод Иконтекстлинк:: Жетдестинатионноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343725"
---
# <a name="icontextlinkgetdestinationnode-method"></a>Метод Иконтекстлинк:: Жетдестинатионноде

Извлекает объект [**иконтекстноде**](icontextnode.md) , который является назначением для этого [**иконтекстлинк**](icontextlink.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдстконтекстнодеид* \[ заполняет\]
</dt> <dd>

Указатель на объект [**иконтекстноде**](icontextnode.md) , который является назначением для этого [**иконтекстлинк**](icontextlink.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппдстконтекстнодеид* , когда больше не нужно использовать узел назначения.

 

Если объект [**иконтекстлинк**](icontextlink.md) связан между узлом, который содержит запись, и узлом, содержащим рисование, узел назначения обычно является узлом, содержащим запись.

Если объект [**иконтекстлинк**](icontextlink.md) имеет тип ссылки, включающий (см. [**Иконтекстлинк:: жетконтекстлинкдиректион**](icontextlink-getcontextlinkdirection.md)), то узел назначения является объектом [**иконтекстноде**](icontextnode.md) , который является вложенным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстлинк**](icontextlink.md)
</dt> <dt>

[**Иконтекстлинк:: Жетсаурценоде**](icontextlink-getsourcenode.md)
</dt> <dt>

[**контекстлинкдиректион**](contextlinkdirection.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

