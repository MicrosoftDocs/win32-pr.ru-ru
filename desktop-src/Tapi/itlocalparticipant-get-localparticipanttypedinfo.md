---
description: Метод Get \_ локалпартиЦипанттипединфо получает сведения о участнике, такие как имя электронной почты или географическое расположение.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'Метод ИтлокалпартиЦипант:: get_LocalParticipantTypedInfo (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41afb4c55ba769e341b81e5ec1ca721745509ba8bf2bdfd88ae22ebc48bb535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003372"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>Метод ИтлокалпартиЦипант:: Get \_ локалпартиЦипанттипединфо

Метод **Get \_ локалпартиЦипанттипединфо** получает сведения о участнике, такие как имя электронной почты или географическое расположение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Инфотипе* \[ окне\]
</dt> <dd>

[**Участник \_ ТИПИЗИРОВАНный \_**](participant-typed-info.md) идентификатор сведений о требуемом типе сведений.

</dd> <dt>

*ппинфо* \[ заполняет\]
</dt> <dd>

Указатель на **BSTR** , который будет содержать необходимые сведения после успешного возврата метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Приложение должно использовать [сисфристринг](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппинфо* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|---------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                                 |
| Заголовок<br/>       | <dl> <dt>Конфприв. h</dt> </dl> |
| Библиотека<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итлокалпартиЦипант**](itlocalparticipant.md)
</dt> <dt>

[**\_сведения о введенных участниках \_**](participant-typed-info.md)
</dt> </dl>

 

