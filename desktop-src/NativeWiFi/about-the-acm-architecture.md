---
description: Сведения об архитектуре ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Сведения об архитектуре ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272463"
---
# <a name="about-the-acm-architecture"></a><span data-ttu-id="f286a-103">Сведения об архитектуре ACM</span><span class="sxs-lookup"><span data-stu-id="f286a-103">About the ACM Architecture</span></span>

<span data-ttu-id="f286a-104">Модуль автоматической настройки (ACM) — это новый компонент настройки беспроводной связи для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f286a-104">The Auto Configuration Module (ACM) is the new wireless configuration component for Windows Vista.</span></span> <span data-ttu-id="f286a-105">В Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2) вместо нее используется служба беспроводной настройки (ВЗК).</span><span class="sxs-lookup"><span data-stu-id="f286a-105">Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) use the Wireless Zero Configuration (WZC) service instead.</span></span>

<span data-ttu-id="f286a-106">ACM периодически сканирует сети и использует итеративный процесс для выбора и подключения к наиболее предпочтительной сети в диапазоне, если в этой сети включен интерфейс для автоматического подключения.</span><span class="sxs-lookup"><span data-stu-id="f286a-106">The ACM scans networks periodically and uses an iterative process to select and connect to the most preferred network in the range, if that network has an interface enabled for auto-connection.</span></span> <span data-ttu-id="f286a-107">ACM также сохраняет и извлекает сетевые профили, которые содержат ACM, модуль MSM, безопасность и независимые поставщики оборудования (IHV).</span><span class="sxs-lookup"><span data-stu-id="f286a-107">The ACM also saves and retrieves network profiles, which contain ACM, Media Specific Module (MSM), security, and independent hardware vendor (IHV) settings.</span></span> <span data-ttu-id="f286a-108">Эти профили сети предназначены для автоматической настройки.</span><span class="sxs-lookup"><span data-stu-id="f286a-108">These network profiles are for auto configuration.</span></span>

<span data-ttu-id="f286a-109">Автоматическая настройка поддерживает как глобальные, так и параметры для каждого интерфейса и сетевые профили.</span><span class="sxs-lookup"><span data-stu-id="f286a-109">Auto configuration supports both global and per-interface settings and network profiles.</span></span> <span data-ttu-id="f286a-110">Глобальные параметры и сетевые профили настраиваются, если компьютер присоединился к домену с объектом групповой политики (GPO) на уровне домена или на уровне подразделения (OU) в иерархии Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="f286a-110">The global settings and network profiles are configured if the machine has joined a domain with a group policy object (GPO) either at the domain level or the organizational unit (OU) level in the Active Directory (AD) hierarchy.</span></span> <span data-ttu-id="f286a-111">Эти параметры и профили групповой политики доступны только для чтения, применяются к каждому интерфейсу 802,11 в системе и всегда имеют приоритет над параметрами для каждого интерфейса и пользователя и сетевыми профилями.</span><span class="sxs-lookup"><span data-stu-id="f286a-111">These group policy settings and profiles are read-only, applied to each 802.11 interface in the system, and always take precedence over the per-interface and per-user settings and network profiles.</span></span> <span data-ttu-id="f286a-112">Профили групповой политики размещаются в верхней части списка предпочтительных сетевых профилей для каждого сетевого интерфейса 802,11.</span><span class="sxs-lookup"><span data-stu-id="f286a-112">The group policy profiles are placed at the top of the preferred network profile list on each 802.11 network interface.</span></span>

<span data-ttu-id="f286a-113">Архитектура ACM является расширяемой.</span><span class="sxs-lookup"><span data-stu-id="f286a-113">The ACM architecture is extensible.</span></span> <span data-ttu-id="f286a-114">Независимые поставщики оборудования могут реализовать собственные беспроводные функции, не изменяя предоставленную собственную платформу 802,11.</span><span class="sxs-lookup"><span data-stu-id="f286a-114">IHVs can implement proprietary wireless functionality without altering the provided native 802.11 framework.</span></span> <span data-ttu-id="f286a-115">Предоставляемые функции и структуры управления IHV позволяют реализовать эту расширяемость.</span><span class="sxs-lookup"><span data-stu-id="f286a-115">The exposed IHV control functions and structures enable this extensibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f286a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f286a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f286a-117">О встроенных WiFi</span><span class="sxs-lookup"><span data-stu-id="f286a-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 



