---
description: Это свойство Mode объекта Session. Это значение, представляющее назначенный флаг режима для текущего сеанса установки. Большинство флагов режима доступны только для чтения извне, но также можно установить несколько заданных флагов.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Свойство Session. Mode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed0c24280307cf368239ab88b5357924a3ee40d5a62444838e155aca2c0642f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629124"
---
# <a name="sessionmode-property"></a>Свойство Session. Mode

Это свойство **mode** объекта [**Session**](session-object.md) . Это значение, представляющее назначенный флаг режима для текущего сеанса установки. Большинство флагов режима доступны только для чтения извне, но также можно установить несколько заданных флагов.

Функция [**мсижетмоде**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) возвращает логическое значение true или false, указывающее, задано ли в настоящий момент конкретное свойство, переданное в функцию (true) или не задано (false).

Обратите внимание, что не все значения *флага* режима выполнения доступны при вызове свойства **mode** из отложенного настраиваемого действия. Дополнительные сведения см. в разделе [Получение контекстных сведений для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a>Значение свойства

Обязательное целочисленное значение для флага. Должна быть одной из следующих:



| Имя флага                                                                                                                                                                                                                                                                                                | Значение                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <dt>**мсирунмодеадмин**</dt> <dt>0</dt> </dl>                                              | Установка в режиме администрирования, в противном случае установка продукта.<br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <dt>**мсирунмодеадвертисе**</dt> <dt>1</dt> </dl>                              | Режим объявления установки.<br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <dt>**мсирунмодемаинтенанце**</dt> <dt>2</dt> </dl>                      | База данных режима обслуживания загружена.<br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <dt>**мсирунмодероллбаккенаблед**</dt> <dt>3</dt> </dl>      | Откат включен.<br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <dt>**мсирунмоделоженаблед**</dt> <dt>4</dt> </dl>                          | Файл журнала активен.<br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <dt>**мсирунмодеоператионс**</dt> <dt>5</dt> </dl>                          | Выполнение операций или постановка в очередь.<br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <dt>**мсирунмодеребутатенд**</dt> <dt>6</dt> </dl>                      | Требуется перезагрузка (Устанавливаемая).<br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <dt>**мсирунмодеребутнов**</dt> <dt>7</dt> </dl>                              | Для продолжения установки требуется перезагрузка (Устанавливаемая).<br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <dt>**мсирунмодекабинет**</dt> <dt>8</dt> </dl>                                      | Установка файлов из ящиков и файлов с помощью таблицы Media.<br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <dt>**мсирунмодесаурцешортнамес**</dt> <dt>9</dt> </dl>  | Исходные файлы используют только короткие имена файлов.<br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <dt>**мсирунмодетаржетшортнамес**</dt> <dt>10</dt> </dl> | В качестве целевых файлов следует использовать только короткие имена файлов.<br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <dt>**msiRunModeWindows9x**</dt> <dt>12</dt> </dl>                             | операционная система — Windows 98/95.<br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <dt>**мсирунмодезавенаблед**</dt> <dt>13</dt> </dl>                         | Операционная система поддерживает рекламу продуктов.<br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <dt>**мсирунмодесчедулед**</dt> <dt>16</dt> </dl>                             | Отложенное [настраиваемое действие](custom-actions.md) , вызываемое из установки выполнения скрипта.<br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <dt>**мсирунмодероллбакк**</dt> <dt>17</dt> </dl>                                 | Отложенное [настраиваемое действие](custom-actions.md) , вызываемое из скрипта выполнения отката.<br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <dt>**мсирунмодекоммит**</dt> <dt>18</dt> </dl>                                         | Отложенное [настраиваемое действие](custom-actions.md) , вызываемое из скрипта выполнения фиксации.<br/>   |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |



 

 




