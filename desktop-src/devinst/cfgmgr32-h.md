---
title: 'Cfgmgr32.h '
description: В этом разделе содержатся справочные разделы по заголовку Cfgmgr32. h.
ms.assetid: 73b4b2ec-ce3d-47c1-9b0e-1052f390ae94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ccc2baf458fea5e20842c9bfa60028c2cb8e23
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "105661783"
---
# <a name="cfgmgr32h"></a>Cfgmgr32.h 

В этом разделе содержатся справочные разделы по заголовку Cfgmgr32. h.

## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_des"><strong>BUSNUMBER_DES</strong></a><br/></td>
<td>Структура BUSNUMBER_DES используется для указания списка ресурсов или требований к ресурсам, описывающих использование номеров шин для экземпляра устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_range"><strong>BUSNUMBER_RANGE</strong></a><br/></td>
<td>Структура BUSNUMBER_RANGE указывает список требований к ресурсам, описывающий использование номеров шин для экземпляра устройства. Дополнительные сведения о списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_resource"><strong>BUSNUMBER_RESOURCE</strong></a><br/></td>
<td>Структура BUSNUMBER_RESOURCE указывает список ресурсов или требования к ресурсам, описывающие использование номеров шин для экземпляра устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a><br/></td>
<td>Функция <strong>CM_Add_Empty_Log_Conf</strong> создает пустую <a href="/windows-hardware/drivers/kernel/hardware-resources">логическую конфигурацию</a>для указанного типа конфигурации и указанного экземпляра устройства на локальном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex"><strong>CM_Add_Empty_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Add_Empty_Log_Conf_Ex</strong> создает пустую <a href="/windows-hardware/drivers/kernel/hardware-resources">логическую конфигурацию</a>для указанного типа конфигурации и указанного экземпляра устройства на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a><br/></td>
<td>Функция <strong>CM_Add_ID</strong> добавляет указанный <a href="/windows-hardware/drivers/install/device-ids">идентификатор устройства</a> (если он еще отсутствует) в список <a href="/windows-hardware/drivers/install/hardware-ids">идентификаторов оборудования</a> <a href="/windows-hardware/drivers/">экземпляра устройства</a> или список <a href="/windows-hardware/drivers/install/compatible-ids">совместимых идентификаторов</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_id_exw"><strong>CM_Add_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Add_ID_Ex</strong> добавляет <a href="/windows-hardware/drivers/install/device-ids">идентификатор устройства</a> (если еще не указано) в список <a href="/windows-hardware/drivers/install/hardware-ids">идентификаторов оборудования</a> экземпляра устройства или список <a href="/windows-hardware/drivers/install/compatible-ids">совместимых идентификаторов</a> на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a><br/></td>
<td>Функция <strong>CM_Add_Res_Des</strong> добавляет <a href="/windows-hardware/drivers/">дескриптор ресурса</a> в <a href="/windows-hardware/drivers/kernel/hardware-resources">логическую конфигурацию</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex"><strong>CM_Add_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Add_Res_Des_Ex</strong> добавляет <a href="/windows-hardware/drivers/">дескриптор ресурса</a> в <a href="/windows-hardware/drivers/kernel/hardware-resources">логическую конфигурацию</a>. Логическая конфигурация может находиться на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_connect_machinew"><strong>CM_Connect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и функций Windows Server 2012 для доступа к удаленным компьютерам, удалено. Не удается получить доступ к удаленным компьютерам при работе в этих версиях Windows.
</blockquote>
<br/> Функция <strong>CM_Connect_Machine</strong> создает подключение к удаленному компьютеру.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_class_key"><strong>CM_Delete_Class_Key</strong></a><br/></td>
<td>Функция <strong>CM_Delete_Class_Key</strong> удаляет указанный класс установленного <a href="/windows-hardware/drivers/">устройства</a> из системы.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a><br/></td>
<td>Функция <strong>CM_Delete_Device_Interface_Key</strong> удаляет подраздел реестра, используемый приложениями и драйверами для хранения сведений, относящихся к интерфейсу.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exa"><strong>CM_Delete_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Delete_Device_Interface_Key_ExA</strong> удаляет подраздел реестра, используемый приложениями и драйверами для хранения сведений, относящихся к интерфейсу.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exw"><strong>CM_Delete_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Delete_Device_Interface_Key_ExW</strong> удаляет подраздел реестра, используемый приложениями и драйверами для хранения сведений, относящихся к интерфейсу.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key"><strong>CM_Delete_DevNode_Key</strong></a><br/></td>
<td>Функция <strong>CM_Delete_DevNode_Key</strong> удаляет указанные разделы реестра, доступные пользователю, связанные с устройством.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disable_devnode"><strong>CM_Disable_DevNode</strong></a><br/></td>
<td>Функция <strong>CM_Disable_DevNode</strong> отключает устройство.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disconnect_machine"><strong>CM_Disconnect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и функций Windows Server 2012 для доступа к удаленным компьютерам, удалено. Не удается получить доступ к удаленным компьютерам при работе в этих версиях Windows.
</blockquote>
<br/> Функция <strong>CM_Disconnect_Machine</strong> удаляет подключение к удаленному компьютеру.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enable_devnode"><strong>CM_Enable_DevNode</strong></a><br/></td>
<td>Функция <strong>CM_Enable_DevNode</strong> включает устройство.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a><br/></td>
<td>Функция <strong>CM_Enumerate_Classes</strong> при повторном вызове перечисляет <a href="/windows-hardware/drivers/">классы установленных устройств</a> на локальном компьютере, предоставляя идентификатор GUID каждого класса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex"><strong>CM_Enumerate_Classes_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Enumerate_Classes_Ex</strong> , при повторном вызове, перечисляет <a href="/windows-hardware/drivers/">классы устройств</a>, установленные на локальном или удаленном компьютере, путем предоставления идентификатора GUID каждого класса.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a><br/></td>
<td>Функция <strong>CM_Enumerate_Enumerators</strong> перечисляет перечислители устройств локального компьютера, указывая имя каждого перечислителя.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exw"><strong>CM_Enumerate_Enumerators_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Enumerate_Enumerators_Ex</strong> перечисляет перечислители устройств локального или удаленного компьютера, указывая имя каждого перечислителя.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a><br/></td>
<td>Функция <strong>CM_Free_Log_Conf</strong> удаляет <a href="/windows-hardware/drivers/kernel/hardware-resources">логическую конфигурацию</a> и все связанные с ними <a href="/windows-hardware/drivers/">дескрипторы ресурсов</a> с локального компьютера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex"><strong>CM_Free_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Free_Log_Conf_Ex</strong> удаляет <a href="/windows-hardware/drivers/kernel/hardware-resources">логическую конфигурацию</a> и все связанные с ними <a href="/windows-hardware/drivers/">дескрипторы ресурсов</a> с локального или удаленного компьютера.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle"><strong>CM_Free_Log_Conf_Handle</strong></a><br/></td>
<td>Функция <strong>CM_Free_Log_Conf_Handle</strong> делает недействительным логический маркер конфигурации и освобождает связанное с ним выделение памяти.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a><br/></td>
<td>Функция <strong>CM_Free_Res_Des</strong> удаляет <a href="/windows-hardware/drivers/">дескриптор ресурса</a> из <a href="/windows-hardware/drivers/kernel/hardware-resources">логической конфигурации</a> на локальном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex"><strong>CM_Free_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Free_Res_Des_Ex</strong> удаляет <a href="/windows-hardware/drivers/">дескриптор ресурса</a> из <a href="/windows-hardware/drivers/kernel/hardware-resources">логической конфигурации</a> либо на локальном, либо на удаленном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle"><strong>CM_Free_Res_Des_Handle</strong></a><br/></td>
<td>Функция <strong>CM_Free_Res_Des_Handle</strong> делает недействительным маркер описания ресурса и освобождает связанное с ним выделение памяти.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_resource_conflict_handle"><strong>CM_Free_Resource_Conflict_Handle</strong></a><br/></td>
<td>Функция <strong>CM_Free_Resource_Conflict_Handle</strong> делает недействительным обработку списка конфликтов ресурсов и освобождает выделение памяти, связанное с маркером.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a><br/></td>
<td>Функция <strong>CM_Get_Child</strong> используется для получения маркера экземпляра устройства в первый дочерний узел указанного узла устройства (<a href="/windows-hardware/drivers/">девноде</a>) в <a href="/windows-hardware/drivers/kernel/device-tree">дереве устройств</a>локального компьютера.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child_ex"><strong>CM_Get_Child_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Child_Ex</strong> используется для получения маркера экземпляра устройства в первый дочерний узел указанного узла устройства (<a href="/windows-hardware/drivers/">девноде</a>) в <a href="/windows-hardware/drivers/kernel/device-tree">дереве устройств</a>локального или удаленного компьютера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a><br/></td>
<td>Функция <strong>CM_Get_Class_Property</strong> извлекает свойство устройства, установленное для класса <a href="/windows-hardware/drivers/install/device-interface-classes">интерфейса устройства</a> или <a href="/windows-hardware/drivers/install/device-setup-classes">класса установки устройства</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_exw"><strong>CM_Get_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Class_Property_ExW</strong> извлекает свойство устройства, установленное для класса <a href="/windows-hardware/drivers/install/device-interface-classes">интерфейса устройства</a> или <a href="/windows-hardware/drivers/install/device-setup-classes">класса установки устройства</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a><br/></td>
<td>Функция <strong>CM_Get_Class_Property_Keys</strong> извлекает массив ключей свойств устройства, которые представляют свойства устройства, заданные для <a href="/windows-hardware/drivers/install/device-interface-classes">класса интерфейса устройства</a> или <a href="/windows-hardware/drivers/install/device-setup-classes">класса установки устройства</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys_ex"><strong>CM_Get_Class_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Class_Property_Keys_Ex</strong> извлекает массив ключей свойств устройства, которые представляют свойства устройства, заданные для <a href="/windows-hardware/drivers/install/device-interface-classes">класса интерфейса устройства</a> или <a href="/windows-hardware/drivers/install/device-setup-classes">класса установки устройства</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw"><strong>CM_Get_Class_Registry_Property</strong></a><br/></td>
<td>Функция <strong>CM_Get_Class_Registry_Property</strong> извлекает <a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">свойство класса установки устройства</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a><br/></td>
<td>Функция <strong>CM_Get_Depth</strong> используется для получения глубины указанного узла устройства (<a href="/windows-hardware/drivers/">девноде</a>) в <a href="/windows-hardware/drivers/kernel/device-tree">дереве устройств</a>локального компьютера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth_ex"><strong>CM_Get_Depth_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Depth_Ex</strong> используется для получения глубины указанного узла устройства (<a href="/windows-hardware/drivers/">девноде</a>) в <a href="/windows-hardware/drivers/kernel/device-tree">дереве устройств</a>локального или удаленного компьютера.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a><br/></td>
<td>Функция <strong>CM_Get_Device_ID</strong> извлекает <a href="/windows-hardware/drivers/install/device-instance-ids">идентификатор экземпляра устройства</a> для указанного <a href="/windows-hardware/drivers/">экземпляра устройства</a> на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_exw"><strong>CM_Get_Device_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Device_ID_Ex</strong> извлекает <a href="/windows-hardware/drivers/install/device-instance-ids">идентификатор экземпляра устройства</a> для указанного <a href="/windows-hardware/drivers/">экземпляра устройства</a> на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a><br/></td>
<td>Функция <strong>CM_Get_Device_ID_List</strong> извлекает список <a href="/windows-hardware/drivers/install/device-instance-ids">идентификаторов экземпляров устройств</a> для <a href="/windows-hardware/drivers/">экземпляров устройств</a>локального компьютера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exw"><strong>CM_Get_Device_ID_List_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Device_ID_List_Ex</strong> извлекает список <a href="/windows-hardware/drivers/install/device-instance-ids">идентификаторов экземпляров устройств</a> для <a href="/windows-hardware/drivers/">экземпляров устройств</a> на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a><br/></td>
<td>Функция <strong>CM_Get_Device_ID_List_Size</strong> Извлекает размер буфера, необходимый для хранения списка <a href="/windows-hardware/drivers/install/device-instance-ids">идентификаторов экземпляров устройств</a> для <a href="/windows-hardware/drivers/">экземпляров устройств</a>локального компьютера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw"><strong>CM_Get_Device_ID_List_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Device_ID_List_Size_Ex</strong> Извлекает размер буфера, необходимый для хранения списка <a href="/windows-hardware/drivers/install/device-instance-ids">идентификаторов экземпляров устройств</a> для локальных или удаленных <a href="/windows-hardware/drivers/">экземпляров устройств</a>на удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a><br/></td>
<td>Функция <strong>CM_Get_Device_ID_Size</strong> Извлекает размер буфера, необходимый для хранения <a href="/windows-hardware/drivers/install/device-instance-ids">идентификатора экземпляра</a> <a href="/windows-hardware/drivers/">устройства на локальном</a> компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex"><strong>CM_Get_Device_ID_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Device_ID_Size_Ex</strong> Извлекает размер буфера, необходимый для хранения <a href="/windows-hardware/drivers/install/device-instance-ids">идентификатора экземпляра</a> <a href="/windows-hardware/drivers/">устройства на локальном</a> или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_aliasw"><strong>CM_Get_Device_Interface_Alias</strong></a><br/></td>
<td>Функция <strong>CM_Get_Device_Interface_Alias</strong> возвращает псевдоним указанного экземпляра интерфейса устройства, если такой псевдоним существует.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a><br/></td>
<td>Функция <strong>CM_Get_Device_Interface_List</strong> извлекает список экземпляров интерфейса устройства, принадлежащих указанному <a href="/windows-hardware/drivers/install/device-interface-classes">классу интерфейса устройства</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea"><strong>CM_Get_Device_Interface_List_Size</strong></a><br/></td>
<td>Функция <strong>CM_Get_Device_Interface_List_Size</strong> Извлекает размер буфера, который должен быть передан функции <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a><br/></td>
<td>Функция <strong>CM_Get_Device_Interface_Property</strong> извлекает свойство устройства, установленное для интерфейса устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_exw"><strong>CM_Get_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Device_Interface_Property_ExW</strong> извлекает свойство устройства, установленное для интерфейса устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a><br/></td>
<td>Функция <strong>CM_Get_Device_Interface_Property_Keys</strong> извлекает массив ключей свойств устройства, которые представляют свойства устройства, заданные для интерфейса устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keys_exw"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Device_Interface_Property_Keys_ExW</strong> извлекает массив ключей свойств устройства, которые представляют свойства устройства, заданные для интерфейса устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a><br/></td>
<td>Функция <strong>CM_Get_DevNode_Property</strong> извлекает свойство экземпляра устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_exw"><strong>CM_Get_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_DevNode_Property_ExW</strong> извлекает свойство экземпляра устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a><br/></td>
<td>Функция <strong>CM_Get_DevNode_Property_Keys</strong> извлекает массив ключей свойств устройства, которые представляют свойства устройства, заданные для экземпляра устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys_ex"><strong>CM_Get_DevNode_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_DevNode_Property_Keys_Ex</strong> извлекает массив ключей свойств устройства, которые представляют свойства устройства, заданные для экземпляра устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_registry_propertyw"><strong>CM_Get_DevNode_Registry_Property</strong></a><br/></td>
<td>Функция <strong>CM_Get_DevNode_Registry_Property</strong> извлекает указанное свойство устройства из реестра.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a><br/></td>
<td>Функция <strong>CM_Get_DevNode_Status</strong> получает состояние экземпляра устройства из узла устройства (<a href="/windows-hardware/drivers/">девноде</a>) в <a href="/windows-hardware/drivers/kernel/device-tree">дереве устройств</a>локального компьютера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex"><strong>CM_Get_DevNode_Status_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_DevNode_Status_Ex</strong> получает состояние экземпляра устройства из узла устройства (<a href="/windows-hardware/drivers/">девноде</a>) в локальном или удаленном <a href="/windows-hardware/drivers/kernel/device-tree">дереве устройств</a>удаленного компьютера.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a><br/></td>
<td>Функция <strong>CM_Get_First_Log_Conf</strong> получает первую <a href="/windows-hardware/drivers/kernel/hardware-resources">логическую конфигурацию</a>указанного типа конфигурации, связанную с указанным <a href="/windows-hardware/drivers/">экземпляром устройства</a> на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex"><strong>CM_Get_First_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_First_Log_Conf_Ex</strong> получает первую <a href="/windows-hardware/drivers/kernel/hardware-resources">логическую конфигурацию</a> , связанную с указанным <a href="/windows-hardware/drivers/">экземпляром устройства</a> , на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa"><strong>CM_Get_HW_Prof_Flags</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей и не должна использоваться.
</blockquote>
<br/> Функция <strong>CM_Get_HW_Prof_Flags</strong> извлекает флаги конфигурации для конкретного <a href="/windows-hardware/drivers/">профиля оборудования</a>для <a href="/windows-hardware/drivers/">экземпляра устройства</a> на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exa"><strong>CM_Get_HW_Prof_Flags_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта функция является устаревшей и не должна использоваться.
</blockquote>
<br/> Функция <strong>CM_Get_HW_Prof_Flags_Ex</strong> извлекает флаги конфигурации для конкретного <a href="/windows-hardware/drivers/">профиля оборудования</a>для <a href="/windows-hardware/drivers/">экземпляра устройства</a> на удаленном компьютере или на локальном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a><br/></td>
<td>Функция <strong>CM_Get_Log_Conf_Priority</strong> получает приоритет конфигурации указанной <a href="/windows-hardware/drivers/kernel/hardware-resources">логической конфигурации</a> на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex"><strong>CM_Get_Log_Conf_Priority_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Log_Conf_Priority_Ex</strong> получает приоритет конфигурации указанной <a href="/windows-hardware/drivers/kernel/hardware-resources">логической конфигурации</a> на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a><br/></td>
<td>Функция <strong>CM_Get_Next_Log_Conf</strong> получает следующую <a href="/windows-hardware/drivers/kernel/hardware-resources">логическую конфигурацию</a> , связанную с конкретным <a href="/windows-hardware/drivers/">экземпляром устройства</a> на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex"><strong>CM_Get_Next_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Next_Log_Conf_Ex</strong> получает следующую <a href="/windows-hardware/drivers/kernel/hardware-resources">логическую конфигурацию</a> , связанную с конкретным <a href="/windows-hardware/drivers/">экземпляром устройства</a> на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a><br/></td>
<td>Функция <strong>CM_Get_Next_Res_Des</strong> получает дескриптор для следующего <a href="/windows-hardware/drivers/">дескриптора ресурса</a>указанного типа ресурса для <a href="/windows-hardware/drivers/kernel/hardware-resources">логической конфигурации</a> на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex"><strong>CM_Get_Next_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Next_Res_Des_Ex</strong> получает дескриптор для следующего <a href="/windows-hardware/drivers/">дескриптора ресурса</a>указанного типа ресурса для <a href="/windows-hardware/drivers/kernel/hardware-resources">логической конфигурации</a> на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a><br/></td>
<td>Функция <strong>CM_Get_Parent</strong> получает маркер экземпляра устройства к родительскому узлу указанного узла устройства (<a href="/windows-hardware/drivers/">девноде</a>) в дереве устройств локального компьютера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent_ex"><strong>CM_Get_Parent_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Parent_Ex</strong> получает маркер экземпляра устройства к родительскому узлу указанного узла устройства (<a href="/windows-hardware/drivers/">девноде</a>) в <a href="/windows-hardware/drivers/kernel/device-tree">дереве устройств</a>локального или удаленного компьютера.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a><br/></td>
<td>Функция <strong>CM_Get_Res_Des_Data</strong> извлекает сведения, хранящиеся в <a href="/windows-hardware/drivers/">дескрипторе ресурса</a> на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex"><strong>CM_Get_Res_Des_Data_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Res_Des_Data_Ex</strong> извлекает сведения, хранящиеся в <a href="/windows-hardware/drivers/">дескрипторе ресурса</a> на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a><br/></td>
<td>Функция <strong>CM_Get_Res_Des_Data_Size</strong> получает размер буфера, необходимый для хранения сведений, содержащихся в указанном <a href="/windows-hardware/drivers/">дескрипторе ресурса</a> на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex"><strong>CM_Get_Res_Des_Data_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Res_Des_Data_Size_Ex</strong> получает размер буфера, необходимый для хранения сведений, содержащихся в указанном <a href="/windows-hardware/drivers/">дескрипторе ресурса</a> на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count"><strong>CM_Get_Resource_Conflict_Count</strong></a><br/></td>
<td>Функция <strong>CM_Get_Resource_Conflict_Count</strong> получает количество конфликтов, содержащихся в указанном списке конфликтов ресурсов.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a><br/></td>
<td>Функция <strong>CM_Get_Resource_Conflict_Details</strong> получает сведения об одном из конфликтов ресурсов в списке конфликтов.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a><br/></td>
<td>Функция <strong>CM_Get_Sibling</strong> получает маркер экземпляра устройства к следующему родственному узлу указанного узла устройства (<a href="/windows-hardware/drivers/">девноде</a>) в <a href="/windows-hardware/drivers/kernel/device-tree">дереве устройств</a>локального компьютера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex"><strong>CM_Get_Sibling_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Get_Sibling_Ex</strong> получает маркер экземпляра устройства к следующему родственному узлу указанного узла устройства в локальном или удаленном <a href="/windows-hardware/drivers/kernel/device-tree">дереве устройств</a>удаленного компьютера.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version"><strong>CM_Get_Version</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей и не должна использоваться.
</blockquote>
<br/> Функция <strong>CM_Get_Version</strong> возвращает версию 4,0 Самонастраивающийся (PnP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) для локального компьютера. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version_ex"><strong>CM_Get_Version_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей и не должна использоваться.
</blockquote>
<br/> Функция <strong>CM_Get_Version_Ex</strong> возвращает версию 4,0 Самонастраивающийся (PnP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) для локального или удаленного компьютера. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a><br/></td>
<td>Функция <strong>CM_Is_Dock_Station_Present</strong> определяет, имеется ли на локальном компьютере <a href="/windows-hardware/drivers/">стыковочный узел</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex"><strong>CM_Is_Dock_Station_Present_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Is_Dock_Station_Present_Ex</strong> определяет, находится ли <a href="/windows-hardware/drivers/">стыковочный узел</a> на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available"><strong>CM_Is_Version_Available</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей и не должна использоваться.
</blockquote>
<br/> Функция <strong>CM_Is_Version_Available</strong> указывает, поддерживается ли заданная версия Самонастраивающийся (PnP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex"><strong>CM_Is_Version_Available_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей и не должна использоваться.
</blockquote>
<br/> Функция <strong>CM_Is_Version_Available_Ex</strong> указывает, поддерживается ли заданная версия САМОНАСТРАИВАЮЩИЙСЯ (PNP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) локальным или удаленным компьютером.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a><br/></td>
<td>Функция <strong>CM_Locate_DevNode</strong> получает в узел устройства обработчик экземпляра устройства, связанный с указанным <a href="/windows-hardware/drivers/install/device-instance-ids">идентификатором экземпляра устройства</a> на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw"><strong>CM_Locate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Locate_DevNode_Ex</strong> получает в узел устройства обработчик экземпляра устройства, связанный с указанным <a href="/windows-hardware/drivers/install/device-instance-ids">идентификатором экземпляра устройства</a>, на локальном компьютере или на удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_mapcrtowin32err"><strong>CM_MapCrToWin32Err</strong></a><br/></td>
<td>Преобразует указанный код <strong>конфигрет</strong> в эквивалентный код системной ошибки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a><br/></td>
<td>Функция <strong>CM_Modify_Res_Des</strong> изменяет указанный дескриптор ресурса на локальном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex"><strong>CM_Modify_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Modify_Res_Des_Ex</strong> изменяет указанный дескриптор ресурса на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ne-cfgmgr32-cm_notify_action"><strong>CM_NOTIFY_ACTION</strong></a><br/></td>
<td>Это перечисление определяет типы событий устройств самонастраивающийся.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_event_data"><strong>CM_NOTIFY_EVENT_DATA</strong></a><br/></td>
<td>Это структура данных события уведомления устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_filter"><strong>CM_NOTIFY_FILTER</strong></a><br/></td>
<td>Структура фильтра уведомлений устройства<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_class_keyw"><strong>CM_Open_Class_Key</strong></a><br/></td>
<td>Функция <strong>CM_Open_Class_Key</strong> открывает раздел реестра класс установки устройства, раздел реестра класса интерфейса устройства или конкретный подраздел класса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a><br/></td>
<td>Функция <strong>CM_Open_Device_Interface_Key</strong> открывает подраздел реестра, используемый приложениями и драйверами для хранения сведений, относящихся к интерфейсу устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya"><strong>CM_Open_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Open_Device_Interface_Key_ExA</strong> открывает подраздел реестра, используемый приложениями и драйверами для хранения сведений, относящихся к интерфейсу устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_key_exw"><strong>CM_Open_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Open_Device_Interface_Key_ExW</strong> открывает подраздел реестра, используемый приложениями и драйверами для хранения сведений, относящихся к интерфейсу устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_devnode_key"><strong>CM_Open_DevNode_Key</strong></a><br/></td>
<td>Функция <strong>CM_Open_DevNode_Key</strong> открывает раздел реестра для сведений о конфигурации для конкретного устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a><br/></td>
<td>Функция <strong>CM_Query_And_Remove_SubTree</strong> проверяет, можно ли удалить экземпляр устройства и его дочерние элементы, и, если это так, удаляет их.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw"><strong>CM_Query_And_Remove_SubTree_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Query_And_Remove_SubTree_Ex</strong> проверяет, можно ли удалить экземпляр устройства и его дочерние элементы, и, если это так, удаляет их.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list"><strong>CM_Query_Resource_Conflict_List</strong></a><br/></td>
<td>Функция <strong>CM_Query_Resource_Conflict_List</strong> определяет экземпляры устройств с требованиями к ресурсам, которые конфликтуют с описанием ресурса указанного экземпляра устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a><br/></td>
<td>Функция <strong>CM_Reenumerate_DevNode</strong> перечисляет устройства, идентифицируемые указанным узлом устройства и всеми его дочерними элементами.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex"><strong>CM_Reenumerate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Reenumerate_DevNode_Ex</strong> перечисляет устройства, идентифицируемые указанным узлом устройства и всеми его дочерними элементами.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a><br/></td>
<td>Используйте <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa"><strong>регистердевиценотификатион</strong></a> вместо <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> , если код предназначен для Windows 7 или более ранних версий Windows. Вместо этого вызывающим объектам в режиме ядра следует использовать <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-ioregisterplugplaynotification"><strong>иорегистерплугплайнотификатион</strong></a> .<br/> Функция <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> регистрирует подпрограммы обратного вызова приложения, вызываемую при возникновении события PnP указанного типа.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a><br/></td>
<td>Функция <strong>CM_Request_Device_Eject</strong> готовит экземпляр локального устройства для безопасного удаления, если устройство является съемным. Если устройство может быть физически извлечено, оно будет иметь значение.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw"><strong>CM_Request_Device_Eject_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Request_Device_Eject_Ex</strong> подготавливает локальный или удаленный экземпляр устройства для безопасного удаления, если устройство является съемным. Если устройство может быть физически извлечено, оно будет иметь значение.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a><br/></td>
<td>Функция <strong>CM_Request_Eject_PC</strong> запрашивает, что портативный компьютер, вставленный в локальную <a href="/windows-hardware/drivers/">станцию стыковки</a>, будет извлечен.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex"><strong>CM_Request_Eject_PC_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Request_Eject_PC_Ex</strong> запрашивает извлечение портативного компьютера, который вставляется в локальную или удаленную <a href="/windows-hardware/drivers/">станцию</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a><br/></td>
<td>Функция <strong>CM_Set_Class_Property</strong> задает свойство класса для класса установки устройства или класса интерфейса устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_property_exw"><strong>CM_Set_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Set_Class_Property_ExW</strong> задает свойство класса для класса установки устройства или класса интерфейса устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertyw"><strong>CM_Set_Class_Registry_Property</strong></a><br/></td>
<td>Функция <strong>CM_Set_Class_Registry_Property</strong> задает или удаляет свойство <a href="/windows-hardware/drivers/install/device-setup-classes">класса установки устройства</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a><br/></td>
<td>Функция <strong>CM_Set_Device_Interface_Property</strong> задает свойство устройства интерфейса устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_property_exw"><strong>CM_Set_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Set_Device_Interface_Property_ExW</strong> задает свойство устройства интерфейса устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a><br/></td>
<td>Функция <strong>CM_Set_DevNode_Problem</strong> задает код проблемы для устройства, установленного на локальном компьютере.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex"><strong>CM_Set_DevNode_Problem_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Set_DevNode_Problem_Ex</strong> задает код проблемы для устройства, установленного на локальном или удаленном компьютере.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a><br/></td>
<td>Функция <strong>CM_Set_DevNode_Property</strong> задает свойство экземпляра устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_property_exw"><strong>CM_Set_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Начиная с Windows 8 и Windows Server 2012, эта функция является устаревшей. Вместо нее используйте <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a> .
</blockquote>
<br/> Функция <strong>CM_Set_DevNode_Property_ExW</strong> задает свойство экземпляра устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw"><strong>CM_Set_DevNode_Registry_Property</strong></a><br/></td>
<td>Функция <strong>CM_Set_DevNode_Registry_Property</strong> задает указанное свойство устройства в реестре.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_setup_devnode"><strong>CM_Setup_DevNode</strong></a><br/></td>
<td>Функция <strong>CM_Setup_DevNode</strong> перезапускает незапущенный экземпляр устройства из-за проблемы с конфигурацией устройства.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_uninstall_devnode"><strong>CM_Uninstall_DevNode</strong></a><br/></td>
<td>Функция <strong>CM_Uninstall_DevNode</strong> удаляет все устойчивое состояние, связанное с экземпляром устройства.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_unregister_notification"><strong>CM_Unregister_Notification</strong></a><br/></td>
<td>Используйте <a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification"><strong>унрегистердевиценотификатион</strong></a> вместо <strong>CM_Unregister_Notification</strong> , если код предназначен для Windows 7 или более ранних версий Windows.<br/> Функция <strong>CM_Unregister_Notification</strong> закрывает указанный обработчик хкмнотификатион.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents"><strong>CMP_WaitNoPendingInstallEvents</strong></a><br/></td>
<td>Функция <strong>CMP_WaitNoPendingInstallEvents</strong> ожидает, пока нет ожидающих действий по установке устройства, которые необходимо выполнить для диспетчера PnP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a"><strong>CONFLICT_DETAILS</strong></a><br/></td>
<td>Структура CONFLICT_DETAILS используется в качестве параметра функции <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_des"><strong>CS_DES</strong></a><br/></td>
<td>Структура CS_DES используется для указания списка ресурсов, описывающего использование ресурсов определенного класса устройств для экземпляра устройства. Дополнительные сведения о списках ресурсов см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_resource"><strong>CS_RESOURCE</strong></a><br/></td>
<td>Структура CS_RESOURCE используется для указания списка ресурсов, описывающего использование ресурсов определенного класса устройств для экземпляра устройства. Дополнительные сведения о списках ресурсов см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_des"><strong>DMA_DES</strong></a><br/></td>
<td>Структура DMA_DES используется для указания списка ресурсов или требований к ресурсам, которые описывают использование канала прямого доступа к памяти (DMA) для экземпляра устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_range"><strong>DMA_RANGE</strong></a><br/></td>
<td>Структура DMA_RANGE указывает список требований к ресурсам, который описывает использование канала DMA для экземпляра устройства. Дополнительные сведения о списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_resource"><strong>DMA_RESOURCE</strong></a><br/></td>
<td>Структура DMA_RESOURCE используется для указания списка ресурсов или требований к ресурсам, которые описывают использование канала DMA для экземпляра устройства. Дополнительные сведения о списках ресурсов и требованиях к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_des"><strong>IO_DES</strong></a><br/></td>
<td>Структура IO_DES используется для указания списка ресурсов или требований к ресурсам, описывающих использование порта ввода-вывода для экземпляра устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_range"><strong>IO_RANGE</strong></a><br/></td>
<td>Структура IO_RANGE указывает список требований к ресурсам, который описывает использование порта ввода-вывода для экземпляра устройства. Дополнительные сведения о списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_resource"><strong>IO_RESOURCE</strong></a><br/></td>
<td>Структура IO_RESOURCE используется для указания списка ресурсов или требований к ресурсам, описывающих использование порта ввода-вывода для экземпляра устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_des_64"><strong>IRQ_DES</strong></a><br/></td>
<td>Структура IRQ_DES используется для указания списка ресурсов или требований к ресурсам, описывающих использование линии IRQ для экземпляра устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_range"><strong>IRQ_RANGE</strong></a><br/></td>
<td>Структура IRQ_RANGE указывает список требований к ресурсам, который описывает использование линии IRQ для экземпляра устройства. Дополнительные сведения о списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_resource_64"><strong>IRQ_RESOURCE</strong></a><br/></td>
<td>Структура IRQ_RESOURCE используется для указания списка ресурсов или требований к ресурсам, описывающих использование линии IRQ для экземпляра устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_des"><strong>MEM_DES</strong></a><br/></td>
<td>Структура MEM_DES используется для указания списка ресурсов или требований к ресурсам, описывающих использование памяти для экземпляра устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_range"><strong>MEM_RANGE</strong></a><br/></td>
<td>Структура MEM_RANGE указывает список требований к ресурсам, который описывает использование памяти для экземпляра устройства. Дополнительные сведения о списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_resource"><strong>MEM_RESOURCE</strong></a><br/></td>
<td>Структура MEM_RESOURCE используется для указания списка ресурсов или требований к ресурсам, описывающих использование памяти для экземпляра устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_des"><strong>MFCARD_DES</strong></a><br/></td>
<td>Структура MFCARD_DES используется для указания списка ресурсов или требований к ресурсам, описывающих использование ресурсов <em>одной</em> из аппаратных функций, предоставляемых экземпляром многофункционального устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_resource"><strong>MFCARD_RESOURCE</strong></a><br/></td>
<td>Структура MFCARD_RESOURCE используется для указания списка ресурсов или требований к ресурсам, описывающих использование ресурсов <em>одной</em> из аппаратных функций, предоставляемых экземпляром многофункционального устройства. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_des"><strong>PCCARD_DES</strong></a><br/></td>
<td>Структура PCCARD_DES используется для указания списка ресурсов или требований к ресурсам, описывающих использование ресурсов экземпляром PC Card. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_resource"><strong>PCCARD_RESOURCE</strong></a><br/></td>
<td>Структура PCCARD_RESOURCE используется для указания списка ресурсов или требований к ресурсам, описывающих использование ресурсов экземпляром PC Card. Дополнительные сведения о списках ресурсов и списках требований к ресурсам см. в разделе <a href="/windows-hardware/drivers/kernel/hardware-resources">ресурсы оборудования</a>.<br/></td>
</tr>
</tbody>
</table>



 

 

 

[Отправить комментарии об этом разделе в Майкрософт](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Cfgmgr32.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Отправить комментарии об этом разделе в Майкрософт")