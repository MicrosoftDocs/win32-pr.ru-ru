---
description: Получает значение, указывающее, является ли объект Иконтекстноде частично заполнен или полностью заполнен.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'Метод Иконтекстноде:: Жетпартиаллипопулатед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b05cb8aae681a7302ae7da40a7412cf828fc159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145529"
---
# <a name="icontextnodegetpartiallypopulated-method"></a>Метод Иконтекстноде:: Жетпартиаллипопулатед

Получает значение, указывающее, является ли объект [**иконтекстноде**](icontextnode.md) частично заполнен или полностью заполнен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфпартиаллипопулатед* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если данный объект [**иконтекстноде**](icontextnode.md) не содержит полных данных. в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Используйте этот метод, если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Дополнительные сведения см. [в разделе Учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

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

[**Иконтекстноде:: Сетпартиаллипопулатед**](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[**Иконтекстноде:: Креатепартиаллипопулатедсубноде**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**\_Ианалисиспроксевентс::P Опулатеконтекстноде**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




