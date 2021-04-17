---
title: Структура MCI_SYSINFO_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс MCI сисинфо содержит сведения для \_ команды MCI сисинфо.'
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- MCI_SYSINFO_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672461"
---
# <a name="mci_sysinfo_parms-structure"></a>\_ \_ Структура пармс MCI сисинфо

Структура **\_ \_ пармс MCI сисинфо** содержит сведения для команды [**MCI \_ сисинфо**](mci-sysinfo.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**лпстрретурн**
</dt> <dd>

Указатель на предоставляемый пользователем буфер для возвращаемой строки. Он также используется для возврата значения **DWORD** при \_ \_ использовании флага MCI сисинфо Quantity.

</dd> <dt>

**двретсизе**
</dt> <dd>

Размер буфера возврата в байтах.

</dd> <dt>

**двнумбер**
</dt> <dd>

Число, указывающее расположение устройства в таблице устройства MCI или в списке открытых устройств, если \_ \_ установлен флаг открытия MCI сисинфо.

</dd> <dt>

**вдевицетипе**
</dt> <dd>

Тип устройства. Этот элемент может быть одним из значений, перечисленных в [типах устройств MCI](mci-device-types.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Структуры MCI**](mci-structures.md)
</dt> <dt>

[**\_СИСИНФО MCI**](mci-sysinfo.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

