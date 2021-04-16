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
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542079"
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

## <a name="remarks"></a>Комментарии

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
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
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

 

