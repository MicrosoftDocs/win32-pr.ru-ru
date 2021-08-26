---
description: Извлекает коллекцию объектов Иконтекстлинк, представляющих связи с другими объектами Иконтекстноде.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'Метод Иконтекстноде:: Жетконтекстлинкс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c3b63e50cf43f06f6065a61dacfbbbd8a00fe7959bb5133407a6c2a980a1a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057843"
---
# <a name="icontextnodegetcontextlinks-method"></a>Метод Иконтекстноде:: Жетконтекстлинкс

Извлекает коллекцию объектов [**иконтекстлинк**](icontextlink.md) , представляющих связи с другими объектами [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппконтекстлинкс* \[ заполняет\]
</dt> <dd>

Указатель на коллекцию объектов [**иконтекстлинк**](icontextlink.md) , представляющих связи с другими объектами [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстлинкс* , когда больше не нужно использовать коллекцию ссылок контекста.

 

Чтобы получить сведения о связях между родительскими или дочерними узлами, используйте [**иконтекстноде:: жетпарентноде**](icontextnode-getparentnode.md) или [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md).

Дополнительные сведения о видах связей, описываемых ссылками, см. в разделе [**иконтекстлинк**](icontextlink.md) и [**контекстлинкдиректион**](contextlinkdirection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**иконтекстлинк**](icontextlink.md)
</dt> <dt>

[**контекстлинкдиректион**](contextlinkdirection.md)
</dt> <dt>

[**Иконтекстноде:: Аддконтекстлинк**](icontextnode-addcontextlink.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

