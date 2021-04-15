---
description: Снимает эксклюзивное использование подключенной смарт-карты.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'Метод Искардманаже:: Скардунлокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263944"
---
# <a name="iscardmanagescardunlock-method"></a>Метод Искардманаже:: Скардунлокк

\[Метод **скардунлокк** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **скардунлокк** освобождает эксклюзивное использование подключенной [*смарт-карты*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Расстановка* \[ окне\]
</dt> <dd>

Состояние для выхода смарт-карты при снятии блокировки.

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

**ВЫХОДА**
</dt><span id="RESET"></span><span id="reset"></span><dt>

**RESET**
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

**Непитание**
</dt><span id="EJECT"></span><span id="eject"></span><dt>

**ВЫДВИНУТ**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                  | Описание                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Operation completed successfully (Операция выполнена успешно).<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *метода обработки* .<br/> |



 

## <a name="remarks"></a>Комментарии

Чтобы заблокировать подключенную смарт-карту, вызовите [**скардлокк**](iscardmanage-scardlock.md).

Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искардманаже**](iscardmanage.md)
</dt> <dt>

[**скардлокк**](iscardmanage-scardlock.md)
</dt> </dl>

 

 
