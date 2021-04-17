---
description: '\_Константы побитового флага фонестате описывают различные элементы состояния для телефонного устройства.'
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: Константы PHONESTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675136"
---
# <a name="phonestate_-constants"></a>\_Константы фонестате

Константы побитового флага **фонестате \_** описывают различные элементы состояния для телефонного устройства.

<dl> <dt>

<span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**ФОНЕСТАТЕ \_ капсчанже**
</dt> <dd> <dl> <dt>



Указывает, что из-за изменений в конфигурации, внесенных пользователем или в других обстоятельствах, изменился один или несколько элементов в структуре [**фонекапс**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) . Приложение должно использовать [**фонежетдевкапс**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) для чтения обновленной структуры. Если поставщик услуг отправляет сообщение о [**\_ состоянии телефона**](phone-state.md) , содержащее это значение, в TAPI, TAPI передает его в приложения с согласованным интерфейсом TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией API, будут получать сообщения о состоянии телефона с \_ указанием фонестате \_ reinit, что требует от них завершения работы и ПОВТОРНОй инициализации подключения к TAPI для получения обновленных сведений.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**ФОНЕСТАТЕ \_ подключен**
</dt> <dd> <dl> <dt>



Подключение между телефонным устройством и TAPI было только что установлено. Это происходит при первом вызове TAPI или при соединении телефонного подключения к компьютеру с помощью TAPI Active.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**ФОНЕСТАТЕ \_ девспеЦифик**
</dt> <dd> <dl> <dt>



Сведения об устройстве, относящиеся к устройству телефона, изменились.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**ФОНЕСТАТЕ \_ отключен**
</dt> <dd> <dl> <dt>



Подключение между телефонным устройством и TAPI было только что разорвано. Это происходит, когда подключение, соединяющее набор телефонов с компьютером, не подключено, пока активен интерфейс TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**ФОНЕСТАТЕ \_ дисплей**
</dt> <dd> <dl> <dt>



Изменился вид телефона.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**ФОНЕСТАТЕ \_ хандсетгаин**
</dt> <dd> <dl> <dt>



Настройка усиления микрофона телефонной трубки изменилась.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**ФОНЕСТАТЕ \_ хандсесуксвитч**
</dt> <dd> <dl> <dt>



Изменилось состояние хуксвитча трубки.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**ФОНЕСТАТЕ \_ хандсетволуме**
</dt> <dd> <dl> <dt>



Параметр громкости динамика телефонной трубки изменился.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**ФОНЕСТАТЕ \_ хеадсесуксвитч**
</dt> <dd> <dl> <dt>



Изменилось состояние хуксвитч гарнитуры.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**ФОНЕСТАТЕ \_ хеадсетгаин**
</dt> <dd> <dl> <dt>



Настройка усиления микрофона для гарнитуры изменена.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**ФОНЕСТАТЕ \_ хеадсетволуме**
</dt> <dd> <dl> <dt>



Параметр громкости динамика гарнитуры изменился.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**\_лампа фонестате**
</dt> <dd> <dl> <dt>



Изменилась лампа телефона.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**\_мониторы фонестате**
</dt> <dd> <dl> <dt>



Число мониторов для телефонного устройства.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**ФОНЕСТАТЕ \_**
</dt> <dd> <dl> <dt>



Phone — изменились элементы состояния, отличные от перечисленных ниже. Приложение должно проверить текущее состояние телефона, чтобы определить, какие элементы были изменены.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**\_владелец фонестате**
</dt> <dd> <dl> <dt>



Число владельцев для телефонного устройства.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**ФОНЕСТАТЕ \_ REinit**
</dt> <dd> <dl> <dt>



Элементы изменились в конфигурации телефонных устройств. Чтобы получать сведения об этих изменениях (как для внешнего вида новых телефонных устройств), приложение должно повторно инициализировать использование TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**ФОНЕСТАТЕ \_ удален**
</dt> <dd> <dl> <dt>



Указывает, что устройство удаляется из системы поставщиком услуг (скорее всего, через действие пользователя, через панель управления или аналогичную служебную программу). Обычно за сообщением о [**\_ состоянии телефона**](phone-state.md) с этим значением будет немедленно следовать сообщение [**\_ закрытия телефона**](phone-close.md) на устройстве. Последующие попытки доступа к устройству до повторной инициализации TAPI приведут к тому, что в \_ приложение будет возвращено устройство фонирр. Если поставщик услуг отправляет \_ сообщение о состоянии телефона, содержащее это значение, в TAPI, TAPI передает его приложениям, имеющим согласованный интерфейс TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией API, не получат уведомлений.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**возобновление ФОНЕСТАТЕ \_**
</dt> <dd> <dl> <dt>



Приложение, используемое для телефонного устройства, будет возобновлено после приостановки в течение некоторого времени.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**ФОНЕСТАТЕ \_ рингмоде**
</dt> <dd> <dl> <dt>



Режим кольца телефона изменился.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**ФОНЕСТАТЕ \_ рингволуме**
</dt> <dd> <dl> <dt>



Громкость звонка на телефоне изменилась.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**ФОНЕСТАТЕ \_ спеакерхуксвитч**
</dt> <dd> <dl> <dt>



Изменилось состояние хуксвитча динамика.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**ФОНЕСТАТЕ \_ спеакергаин**
</dt> <dd> <dl> <dt>



Состояние настройки усиления микрофона динамика изменилось.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**ФОНЕСТАТЕ \_ спеакерволуме**
</dt> <dd> <dl> <dt>



Параметр громкости динамиков динамика изменился.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**Приостановка ФОНЕСТАТЕ \_**
</dt> <dd> <dl> <dt>



Приложение использует телефон временно приостановлено.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_закрытие телефона**](phone-close.md)
</dt> <dt>

[**\_состояние телефона**](phone-state.md)
</dt> <dt>

[**фонекапс**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**фонежетдевкапс**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




