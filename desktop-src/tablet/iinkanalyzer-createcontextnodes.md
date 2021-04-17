---
description: Создает объект Иконтекстнодес.
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'Метод Иинканализер:: Креатеконтекстнодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711117"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a>Метод Иинканализер:: Креатеконтекстнодес

Создает объект [**иконтекстнодес**](icontextnodes.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппконтекстнодес* \[ заполняет\]
</dt> <dd>

Указатель на объект [**иконтекстнодес**](icontextnodes.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодес* , когда больше не нужно использовать объект.

 

Используйте этот метод, чтобы создать пустую коллекцию [**иконтекстнодес**](icontextnodes.md) , связанную с [**иинканализер**](iinkanalyzer.md). Новая коллекция **иконтекстнодес** не является частью дерева контекста объекта **иинканализер** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**иконтекстнодес**](icontextnodes.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

