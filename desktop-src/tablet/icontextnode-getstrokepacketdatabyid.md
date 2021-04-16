---
description: Извлекает массив, содержащий данные свойства пакета для указанного штриха.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'Метод Иконтекстноде:: Жетстрокепаккетдатабид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692444"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a>Метод Иконтекстноде:: Жетстрокепаккетдатабид

Извлекает массив, содержащий данные свойства пакета для указанного штриха.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*строкеид* \[ окне\]
</dt> <dd>

Идентификатор для штриха.

</dd> <dt>

*пстрокепаккетдатакаунт* \[ в, out\]
</dt> <dd>

Длина массива данных пакета.

</dd> <dt>

*пплстрокепаккетдата* \[ заполняет\]
</dt> <dd>

Указатель на данные пакета для штриха.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *пплстрокепаккетдата* , если эта информация больше не нужна.

 

*плстрокепаккетдата* содержит данные пакетов для всех точек в штрихе. Чтобы получить типы данных пакетов, включаемые для каждой точки в штрихе, используйте [**иконтекстноде:: жетстрокепаккетдескриптионбид**](icontextnode-getstrokepacketdescriptionbyid.md).

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

[**Иконтекстноде:: Жетстрокепаккетдескриптионбид**](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

