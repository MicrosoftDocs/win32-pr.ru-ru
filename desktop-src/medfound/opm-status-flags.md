---
description: Флаги в следующей таблице определяют состояние сеанса вывода диспетчера (ОПМ).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Флаги состояния ОПМ (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543855"
---
# <a name="opm-status-flags"></a>Флаги состояния ОПМ

Флаги в следующей таблице определяют состояние сеанса вывода диспетчера (ОПМ).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа/значение</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </dl></td>
<td style="text-align: left;">Нормальное состояние.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </dl></td>
<td style="text-align: left;">Целостность подключения скомпрометирована. Ниже приведены примеры событий, которые вызывают установку драйвером этого флага.<br/>
<ul>
<li>Драйвер больше не может применить текущий уровень защиты.</li>
<li>Драйвер обнаружил внутреннюю ошибку целостности.</li>
<li>Соединитель между компьютером и устройством дисплея был отсоединен.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </dl></td>
<td style="text-align: left;">Конфигурация подключения изменилась. Например, пользователь изменил режим экрана рабочего стола.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </dl></td>
<td style="text-align: left;">Графический адаптер или драйвер были изменены.<br/> Этот флаг не используется в <em>режиме эмуляции Копп</em>. Вместо этого выходные данные видео задают флаг OPM_STATUS_LINK_LOST, если он обнаруживает несанкционированный вызов.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </dl></td>
<td style="text-align: left;">Отозванное High-Bandwidth устройства с цифровой Защита содержимого (HDCP) прикрепляется к выходным данным видео.<br/> Этот флаг состояния может быть возвращен из запроса <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> или <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> . <br/> Отозванное устройство может быть подключено непосредственно к выходным данным видео или косвенно через повторитель HDCP. Для обнаружения этого состояния в то время, когда HDCP включен, требуется вывод видео, но в противном случае — нет.<br/> Этот флаг не используется в <em>режиме эмуляции Копп</em>, так как видеопотокы не обнаруживают отозванные устройства в этом режиме.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Комментарии

Некоторые из этих констант эквивалентны значениям из перечисления **Копп \_ статусфлагс** , используемого в сертифицированном протоколе защиты выходных данных (Копп).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>Опмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления ОПМ](opm-enumerations.md)
</dt> </dl>

 

 




