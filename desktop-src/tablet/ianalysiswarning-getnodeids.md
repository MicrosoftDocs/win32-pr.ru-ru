---
description: Возвращает идентификаторы всех соответствующих узлов контекста, связанных с данным предупреждением.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'Метод Ианалисисварнинг:: Жетнодеидс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 97e6f4fde66faef14402c815f6b95517a2bd19adfb90eac4e865383770bc753f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967483"
---
# <a name="ianalysiswarninggetnodeids-method"></a>Метод Ианалисисварнинг:: Жетнодеидс

Возвращает идентификаторы всех соответствующих узлов контекста, связанных с данным предупреждением.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулкаунт* \[ в, out\]
</dt> <dd>

Число глобально уникальных идентификаторов (GUID) в *ппнодеидс*.

</dd> <dt>

*ппнодеидс* \[ заполняет\]
</dt> <dd>

Указатель на массив идентификаторов GUID, который определяет контекстные узлы, связанные с этим предупреждением анализа, или **значение NULL** , если с предупреждением не связаны контекстные узлы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Если *ппнодеидс* передается как **null**, метод **жетнодеидс** возвращает значение **S \_ ОК** , а число прямоугольников возвращается в *пулкаунт*.

> [!Caution]  
> Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппнодеидс* , если эта информация больше не нужна.

 

## <a name="examples"></a>Примеры

В следующем примере показано, как получить объекты [**иконтекстноде**](icontextnode.md) , которые находятся в [**ианалисисварнинг**](ianalysiswarning.md), `warning` и как получить только число объектов **иконтекстноде**


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ианалисисварнинг**](ianalysiswarning.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Метод Иинканализер:: Финдноде**](iinkanalyzer-findnode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

