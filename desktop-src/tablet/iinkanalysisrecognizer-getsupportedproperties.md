---
description: Получает глобальные уникальные идентификаторы (GUID) для свойств, которые эта Иинканалисисрекогнизер может создать для результатов анализа.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'Метод Иинканалисисрекогнизер:: Жетсуппортедпропертиес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991159"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a>Метод Иинканалисисрекогнизер:: Жетсуппортедпропертиес

Получает глобальные уникальные идентификаторы (GUID) для свойств, которые эта [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) может создать для результатов анализа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулпропертиескаунт* \[ в, out\]
</dt> <dd>

Число идентификаторов GUID в *пппропертиес*.

</dd> <dt>

*пппропертиес* \[ заполняет\]
</dt> <dd>

Указатель на идентификаторы GUID свойств, которые эта [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) может создать для результатов анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *пппропертиес* , если эта информация больше не нужна.

 

Распознаватель может поддерживать линии метрик, Номера строк, уровни достоверности и т. д. Полный список свойств, которые может поддерживать распознаватель, см. в разделе [константы рекогнитионпроперти](recognitionproperty-constants.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканалисисрекогнизер**](iinkanalysisrecognizer.md)
</dt> <dt>

[Константы Рекогнитионпроперти](recognitionproperty-constants.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

