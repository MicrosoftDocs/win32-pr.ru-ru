---
title: Команда index
description: Команда index управляет экраном видеомагнитофона. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: 16066acf-37aa-4bff-b97e-5eb2420ac3c4
keywords:
- Команда index мультимедиа Windows
topic_type:
- apiref
api_name:
- index
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da652b1a7a48dffd9850c435345fcfcb11c2e674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989423"
---
# <a name="index-command"></a>Команда index

Команда index управляет экраном видеомагнитофона. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.

Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("index %s %s %s"), 
  lpszDeviceID, 
  lpszIndex, 
  lpszFlags
); 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*
</dt> <dd>

Идентификатор устройства MCI. Этот идентификатор или псевдоним назначается при открытии устройства.

</dd> <dt>

<span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*лпсзиндекс*
</dt> <dd>

Один из следующих флагов.



| Значение | Значение                                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| off   | Отключает экран.                                                                                         |
| on    | Включает экран на экране. Отображаемый элемент задается с помощью флага "index" команды [Set](set.md) . |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*
</dt> <dd>

Может принимать значение "Wait", "notify" или "Test". Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Строки команд MCI](mci-command-strings.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

