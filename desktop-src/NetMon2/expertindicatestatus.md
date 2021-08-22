---
description: Функция Експертиндикатестатус указывает процент завершения анализа экспертов файла записи.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Функция Експертиндикатестатус (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f9f40e339b450496ec4b0aff1f3e951c4d7468fa22f7b2ff3dd2f84de6b92354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012272"
---
# <a name="expertindicatestatus-function"></a>Функция Експертиндикатестатус

Функция **експертиндикатестатус** указывает процент завершения анализа файла записи экспертом.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хексперткэй* \[ окне\]
</dt> <dd>

Уникальный идентификатор эксперта. Сетевой монитор передает *хексперткэй* эксперту при вызове функции [Run](run.md) .

</dd> <dt>

*Состояние* \[ окне\]
</dt> <dd>

Текущее состояние анализа. Укажите одно из следующих значений [експертстатусенумератион](expertstatusenumeration.md) .



| Значение                                                                                                                                                                                 | Значение                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**ЕКСПЕРТСТАТУС \_ неактивен**</dt> </dl> | Эксперт никогда не начал работу. <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**ЕКСПЕРТСТАТУС \_ Запуск**</dt> </dl> | Эксперт начинает работу. <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**ЕКСПЕРТСТАТУС \_ работает**</dt> </dl>    | Эксперт работает нормально. <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**\_проблема експертстатус**</dt> </dl>    | Проблема, указанная в параметре подсостояния, прекратила работу эксперта. <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**ЕКСПЕРТСТАТУС \_ прервана**</dt> </dl>    | Сетевой монитор был остановлен эксперт. <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**ЕКСПЕРТСТАТУС \_ Готово**</dt> </dl>             | Эксперт успешно завершил анализ. <br/>                     |



 

</dd> <dt>

*Подсостояние* \[ окне\]
</dt> <dd>

Расширение или уточнение сведений, предоставленных параметром *Status* .

</dd> <dt>

*сзтекст* \[ окне\]
</dt> <dd>

Необязательный индикатор состояния текста.

Значение этого параметра может быть **равно NULL**.

</dd> <dt>

*PercentDone* \[ заполняет\]
</dt> <dd>

Процент данных записи, обработанных экспертом.

Когда эксперт успешно завершает анализ файла записи, система устанавливает в процентах значение 100. Любое число больше 99 будет игнорироваться.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР Expert ( \_ эксперт). \_ эксперт должен немедленно очистить и вернуться, не выполняя захват.

## <a name="remarks"></a>Remarks

Функция **експертиндикатестатус** может вызываться экспертами, реализующими функцию [запуска](run.md) или [настройки](configure.md) экспорта.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
