---
description: Извлекает массив, содержащий идентификаторы свойств пакета для указанного росчерка.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'Метод Иконтекстноде:: Жетстрокепаккетдескриптионбид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692443"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a>Метод Иконтекстноде:: Жетстрокепаккетдескриптионбид

Извлекает массив, содержащий идентификаторы свойств пакета для указанного росчерка.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лстрокеид* \[ окне\]
</dt> <dd>

Идентификатор для штриха.

</dd> <dt>

*пулстрокепаккетдескриптионкаунт* \[ в, out\]
</dt> <dd>

Число свойств пакетов в каждом пакете.

</dd> <dt>

*ппстрокепаккетдескриптионгуидс* \[ заполняет\]
</dt> <dd>

Массив, содержащий идентификаторы свойств пакета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппстрокепаккетдескриптионгуидс* , если эта информация больше не нужна.

 

\**ппстрокепаккетдескриптионгуидс* содержит глобальные уникальные идентификаторы (GUID), которые описывают типы данных пакетов, включаемые для каждой точки в штрихе. Полный список доступных свойств пакетов см. в разделе [константы паккетпропертигуидс](packetpropertyguids-constants.md).

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

[**Иконтекстноде:: Жетстрокепаккетдатабид**](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

