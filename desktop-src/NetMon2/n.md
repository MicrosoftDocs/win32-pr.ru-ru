---
description: Глоссарий терминов сетевой монитор, начинающихся с буквы N.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: N (сетевой монитор)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881fb15f4432f6d2bb4b92025c28fc88c1862fa018e9e01df06c5ea8e79ced53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555794"
---
# <a name="n-network-monitor"></a>N (сетевой монитор)

<dl> <dt>

<span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**АДАПТЕР**
</dt> <dd>

См. спецификацию интерфейса сетевого драйвера.

</dd> <dt>

<span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**Спецификация интерфейса сетевого драйвера (NDIS)**
</dt> <dd>

Спецификация интерфейса между драйверами устройств и сетью. Все транспорты вызывают интерфейс NDIS для доступа к картам сетевых интерфейсов и работы с ними.

</dd> <dt>

<span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Агент сетевой монитор**
</dt> <dd>

Компонент сетевой монитор. Агент позволяет удаленному компьютеру записывать данные из сети. При удаленной установке сетевой монитор к агенту сетевой монитор и инициирует запись, статистика из записи передается по сети на управляющий компьютер. Перемещение продолжается с интервалов, указанных при установке соединения.

</dd> <dt>

<span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**Поставщик сетевых пакетов (НПП)**
</dt> <dd>

Компонент сетевой монитор, собирающий сетевой трафик в кадрах, а затем передающий кадры эксперту и НПП приложение. НПП использует драйвер сетевой монитор системы (Nmnt.sys) для получения кадров, собранных из сети, и предоставляет несколько COM-интерфейсов, которые передают кадры эксперту, монитору и в приложение поставщика сетевых пакетов (НПП), где их можно просматривать и анализировать.

</dd> <dt>

<span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**нпп**
</dt> <dd>

См. раздел поставщик сетевых пакетов.

</dd> <dt>

<span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**Приложение НПП**
</dt> <dd>

Приложение, которое обходит как средство управления сетевой монитор пользовательского интерфейса, так и монитор, и напрямую подключается к поставщику сетевых пакетов (НПП). Приложение НПП может подключаться к компоненту НПП с помощью любого из пяти интерфейсов COM НПП.

</dd> <dt>

<span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**НПП Finder**
</dt> <dd>

Компонент сетевой монитор, взаимодействующий с НППС.

</dd> </dl>

 

 



