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
ms.openlocfilehash: 2fab5b5fce4d87c32fb3435fdad2cfc6b126069b40c7e5c7c2fb302ee468e480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773804"
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

## <a name="remarks"></a>Remarks

Используйте этот метод, если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Дополнительные сведения см. [в разделе Учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
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

 

 




