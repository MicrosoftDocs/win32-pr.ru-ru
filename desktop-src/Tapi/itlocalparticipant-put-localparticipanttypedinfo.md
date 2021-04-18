---
description: Метод размещения \_ локалпартиЦипанттипединфо задает сведения о участнике.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: 'ИтлокалпартиЦипант: метод ut_LocalParticipantTypedInfo:p (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689070"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a>ИтлокалпартиЦипант::p UT \_ локалпартиЦипанттипединфо метод

Метод **размещения \_ локалпартиЦипанттипединфо** задает сведения о участнике.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Инфотипе* \[ окне\]
</dt> <dd>

[**Участник \_ ТИПИЗИРОВАНный \_**](participant-typed-info.md) идентификатор сведений о требуемом типе информации.

</dd> <dt>

*ппинфо* \[ окне\]
</dt> <dd>

**BSTR** , содержащий необходимое новое значение для данных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Приложение должно использовать [сисаллокстринг](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Ппинфо* и использовать [сисфристринг](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|---------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                                 |
| Header<br/>       | <dl> <dt>Конфприв. h</dt> </dl> |
| Библиотека<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итлокалпартиЦипант**](itlocalparticipant.md)
</dt> <dt>

[**\_сведения о введенных участниках \_**](participant-typed-info.md)
</dt> </dl>

 

