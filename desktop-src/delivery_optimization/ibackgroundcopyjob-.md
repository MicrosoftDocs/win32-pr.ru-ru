---
title: Интерфейс использованием метода ibackgroundcopyjob (Deliveryoptimization. h)
description: Используйте интерфейс использованием метода ibackgroundcopyjob для добавления файлов в задание, задания уровня приоритета задания, определения состояния задания, а также для запуска и завершения задания.
ms.assetid: 0D1EAC8D-0013-4FBC-A07F-14CD5D709549
keywords:
- Интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04572f11afd51c3354c5adabd9950e2a3942287a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071534"
---
# <a name="ibackgroundcopyjob-interface"></a>Интерфейс использованием метода ibackgroundcopyjob

Используйте интерфейс [**использованием метода ibackgroundcopyjob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) для добавления файлов в задание, задания уровня приоритета задания, определения состояния задания, а также для запуска и завершения задания.

Чтобы создать задание, вызовите метод [**ибаккграундкопиманажер:: CreateJob**](ibackgroundcopymanager-createjob.md) . Чтобы получить указатель интерфейса [**использованием метода ibackgroundcopyjob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) на существующее задание, вызовите метод [**Ибаккграундкопиманажер:: жетжоб**](ibackgroundcopymanager-getjob.md) .

## <a name="members"></a>Элементы

Интерфейс **использованием метода ibackgroundcopyjob** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Использованием метода ibackgroundcopyjob** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **использованием метода ibackgroundcopyjob** содержит следующие методы.



| Метод                                                                  | Описание                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Отменить**](ibackgroundcopyjob-cancel.md)                             | Отменяет задание и удаляет временные файлы с клиента.<br/>                                                                                                                                                           |
| [**Завершить**](ibackgroundcopyjob-complete.md)                         | Завершает задание и сохраняет перенесенные файлы на клиенте.<br/>                                                                                                                                                            |
| [**енумфилес**](ibackgroundcopyjob-enumfiles.md)                       | Возвращает указатель интерфейса на объект перечислителя, который используется для перечисления файлов в задании.<br/>                                                                                                                   |
| [**Переdisplayname**](ibackgroundcopyjob-getdisplayname.md)             | Извлекает отображаемое имя, идентифицирующее задание.<br/>                                                                                                                                                                    |
| [**Ошибка**](ibackgroundcopyjob-geterror.md)                         | Извлекает указатель интерфейса на объект ошибки после возникновения ошибки.<br/>                                                                                                                                              |
| [**GetId**](ibackgroundcopyjob-getid.md)                               | Возвращает идентификатор задания в очереди.<br/>                                                                                                                                                                      |
| [**жетнопрогресстимеаут**](ibackgroundcopyjob-getnoprogresstimeout.md) | Возвращает продолжительность времени, в течение которого будет выполняться попытка пересылки файла после возникновения временной ошибки.<br/>                                                                                             |
| [**жетнотифифлагс**](ibackgroundcopyjob-getnotifyflags.md)             | Получает флаги уведомления о событиях (обратный вызов), заданные для приложения.<br/>                                                                                                                                   |
| [**жетнотифинтерфаце**](ibackgroundcopyjob-getnotifyinterface.md)     | Извлекает указатель на реализацию интерфейса [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) (обратные вызовы).<br/>                                                                                    |
| [**GetPriority**](ibackgroundcopyjob-getpriority.md)                   | Возвращает уровень приоритета, заданный для задания.<br/>                                                                                                                                                                 |
| [**GetProgress**](ibackgroundcopyjob-getprogress.md)                   | Извлекает сведения о ходе выполнения, связанные с заданием, такие как число байтов и файлов, передаваемых клиенту.<br/>                                                                                                           |
| [**GetState**](ibackgroundcopyjob-getstate.md)                         | Возвращает состояние задания.<br/>                                                                                                                                                                                        |
| [**Время ожидания**](ibackgroundcopyjob-gettimes.md)                         | Возвращает метки времени для действий, связанных с заданием, например время создания задания.<br/>                                                                                                                         |
| [**GetType**](ibackgroundcopyjob-gettype.md)                           | Возвращает тип выполняемой пересылки, например скачивание файла.<br/>                                                                                                                                               |
| [**Возобновить**](ibackgroundcopyjob-resume.md)                             | Запускает новое задание или перезапускает приостановленное задание.<br/>                                                                                                                                                                          |
| [**сетнопрогресстимеаут**](ibackgroundcopyjob-setnoprogresstimeout.md) | Указывает период времени, в течение которого будет выполняться попытка пересылки файла после возникновения временной ошибки.<br/>                                                                                             |
| [**сетнотифифлагс**](ibackgroundcopyjob-setnotifyflags.md)             | Указывает тип уведомления о событии для получения.<br/>                                                                                                                                                                   |
| [**сетнотифинтерфаце**](ibackgroundcopyjob-setnotifyinterface.md)     | Указывает указатель на реализацию интерфейса [**ибаккграундкопикаллбакк**](ibackgroundcopycallback.md) (обратные вызовы). Интерфейс получает уведомления на основе заданных флагов уведомления о событиях.<br/> |
| [**SetPriority**](ibackgroundcopyjob-setpriority.md)                   | Указывает приоритет задания относительно других заданий в очереди обмена.<br/>                                                                                                                                        |
| [**Анализируем**](ibackgroundcopyjob-suspend.md)                           | Приостанавливает задание.<br/>                                                                                                                                                                                                        |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкопифиле**](ibackgroundcopyfile.md)
</dt> <dt>

[**ибаккграундкопиманажер**](ibackgroundcopymanager.md)
</dt> </dl>

 

