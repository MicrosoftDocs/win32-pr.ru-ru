---
description: Собственные разрешения API WiFi
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: Собственные разрешения API WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afafec7619e0920a17e3769a430c8c79aeff3828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264379"
---
# <a name="native-wifi-api-permissions"></a>Собственные разрешения API WiFi

Неуправляемый вызов API WiFi может завершиться ошибкой, если вызывающий объект не имеет достаточных разрешений для выполнения запрошенной операции.

Разрешения хранятся в [списках управления доступом на уровне пользователей (DACL)](../secauthz/access-control-lists.md) , связанных с [**\_ защищаемым \_ объектом WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object). Дополнительные сведения о DACL и защищаемых объектах см. [в статье Управление доступом к объекту в DACL](../secauthz/how-dacls-control-access-to-an-object.md).

В следующей таблице показаны собственные функции WiFi, использующие защищаемые объекты для определения наличия у вызывающего объекта достаточных разрешений для выполнения запрошенной операции. В нем также показаны защищаемые объекты, используемые каждой функцией.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Защищаемый объект</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>Вланжетфилтерлист</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>влансетфилтерлист</strong></a><br/></td>
<td><ul>
<li>wlan_secure_deny_list</li>
<li>wlan_secure_permit_list</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>вланихвконтрол</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ihv_control</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>Вланкуеряутоконфигпараметер</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>влансетаутоконфигпараметер</strong></a><br/></td>
<td><ul>
<li>wlan_secure_show_denied</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>Вланкуеринтерфаце</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>влансетинтерфаце</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ac_enabled</li>
<li>wlan_secure_bc_scan_enabled</li>
<li>wlan_secure_bss_type</li>
<li>wlan_secure_current_operation_mode</li>
<li>wlan_secure_interface_properties</li>
<li>wlan_secure_media_streaming_mode_enabled</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>влансетпрофиле</strong></a><br/></td>
<td><ul>
<li>wlan_secure_add_new_all_user_profiles</li>
<li>wlan_secure_add_new_per_user_profiles</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>Влансетпрофилелист</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>влансетпрофилепоситион</strong></a><br/></td>
<td><ul>
<li>wlan_secure_all_user_profiles_order</li>
</ul></td>
</tr>
</tbody>
</table>



 

Прежде чем одна из указанных выше функций завершит свою работу, она получает список DACL, хранящийся в соответствующем защищаемом объекте. Затем функция проверяет DACL, чтобы узнать, достаточно ли у вызывающего объекта разрешений. Для \* функций вланжет и вланкуери \* требуется, чтобы список DACL содержал [запись управления доступом (ACE)](../secauthz/access-control-entries.md) , которая предоставляет [маркер доступа](../secauthz/access-tokens.md) вызывающему потоку \_ доступ на чтение \_ для функции WLAN. \*Функциям набора WLAN требуется ACE, который предоставляет маркер доступа для доступа на запись WLAN вызывающего потока \_ \_ . Если вызывающий объект не имеет достаточных разрешений, вызов функции завершится ошибкой с ошибкой " \_ доступ \_ запрещен".

С каждым защищаемым объектом связан список DACL по умолчанию. Разрешения по умолчанию, хранящиеся в списке DACL, можно изменить с помощью функции [**влансетсекуритисеттингс**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) . Чтобы определить действующие права пользователя, необходимые для выполнения операции в определенной системе, вызовите [**вланжетсекуритисеттингс**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Профили всех пользователей имеют дополнительные разрешения, связанные с самим профилем. Разрешения для профиля "все пользователи" устанавливаются при создании или изменении профиля с помощью [**влансетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) или [**влансаветемпорарипрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile). Параметр *страллусерпрофилесекурити* указывает необходимые разрешения для изменения профиля, удаления профиля или подключения к сети с помощью профиля. Для удаления или изменения профиля требуется \_ разрешение на запись WLAN \_ . Для подключения к сети, использующей профиль, требуется разрешение на выполнение беспроводной сети \_ \_ .

* * Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2): * * функции [**вланжетсекуритисеттингс**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) и [**влансетсекуритисеттингс**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) не поддерживаются. Параметр *страллусерпрофилесекурити* не используется.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Управление доступом к объекту с помощью списков DACL](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**\_защищаемый \_ объект WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
