---
title: Ведение журнала (платформа фильтрации Windows)
description: Платформа фильтрации Windows (WFP) обеспечивает ведение журнала отказов пакетов и IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105661809"
---
# <a name="logging-windows-filtering-platform"></a><span data-ttu-id="a70f0-103">Ведение журнала (платформа фильтрации Windows)</span><span class="sxs-lookup"><span data-stu-id="a70f0-103">Logging (Windows Filtering Platform)</span></span>

<span data-ttu-id="a70f0-104">Платформа фильтрации Windows (WFP) обеспечивает ведение журнала отказов пакетов и IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="a70f0-104">The Windows Filtering Platform (WFP) provides logging of packet drops and IKE/AuthIP failures.</span></span>

<span data-ttu-id="a70f0-105">Записанные в журнал события определяются в перечислимом типе [**фвпм \_ net \_ event \_ Type**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) и имеют следующие значения.</span><span class="sxs-lookup"><span data-stu-id="a70f0-105">The logged events are defined in the [**FWPM\_NET\_EVENT\_TYPE**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) enumerated type and are as follows.</span></span>

-   <span data-ttu-id="a70f0-106">Сбои в основном режиме IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="a70f0-106">IKE/AuthIP main mode failures.</span></span>
-   <span data-ttu-id="a70f0-107">Сбои быстрого режима IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="a70f0-107">IKE/AuthIP quick mode failures.</span></span>
-   <span data-ttu-id="a70f0-108">Сбои расширенного режима AuthIP.</span><span class="sxs-lookup"><span data-stu-id="a70f0-108">AuthIP extended mode failures.</span></span>
-   <span data-ttu-id="a70f0-109">Пакеты, отброшенные во время классификации.</span><span class="sxs-lookup"><span data-stu-id="a70f0-109">Packets dropped during classification.</span></span>
-   <span data-ttu-id="a70f0-110">Пакеты, отброшенные протоколом IPsec.</span><span class="sxs-lookup"><span data-stu-id="a70f0-110">Packets dropped by IPsec.</span></span>

<span data-ttu-id="a70f0-111">По умолчанию ведение журнала WFP включено для одноадресных входящих пакетов и для всех исходящих пакетов (одноадресный, многоадресный и широковещательный).</span><span class="sxs-lookup"><span data-stu-id="a70f0-111">By default, logging for WFP is enabled for unicast inbound packets and for all outbound packets (unicast, multicast, and broadcast).</span></span> <span data-ttu-id="a70f0-112">Ведение журнала может быть включено для остальных пакетов или отключено для всех пакетов с помощью функции управления [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) .</span><span class="sxs-lookup"><span data-stu-id="a70f0-112">Logging can be enabled for the rest of the packets, or disabled for all packets, through the [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) management function.</span></span> <span data-ttu-id="a70f0-113">Параметры событий сохраняются во всех перезагрузках.</span><span class="sxs-lookup"><span data-stu-id="a70f0-113">Event settings persist across reboots.</span></span>

<span data-ttu-id="a70f0-114">Записанные в журнал события хранятся в цикле, то есть новые события переопределяют старые, когда размер журнала достигает максимального размера, и его можно проанализировать с помощью функций [управления событиями](fwp-mgmt-functions.md) , предоставляемых WFP.</span><span class="sxs-lookup"><span data-stu-id="a70f0-114">Logged events are stored in a circular log, that is new events override old ones when the log reaches its maximum size, and can be analyzed using the [event management](fwp-mgmt-functions.md) functions provided by WFP.</span></span> <span data-ttu-id="a70f0-115">Максимальный размер журнала событий составляет 128 КБ. он может содержать около 100 в 150 событий.</span><span class="sxs-lookup"><span data-stu-id="a70f0-115">The event log has a maximum size of 128 KB and it can hold about 100 to 150 events.</span></span>

<span data-ttu-id="a70f0-116">Функции перечисления в целом и [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) в частности, сделайте моментальный снимок журнала во время создания маркера перечисления.</span><span class="sxs-lookup"><span data-stu-id="a70f0-116">Enumeration functions in general, and [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)/[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) in particular, take a snapshot of the log at the time the enumeration handle is created.</span></span> <span data-ttu-id="a70f0-117">Последующие вызовы, использующие один и тот же маркер перечисления, возвращают следующий набор элементов, следующих за последним выходным буфером.</span><span class="sxs-lookup"><span data-stu-id="a70f0-117">Subsequent calls using the same enumeration handle return the next set of items following those in the last output buffer.</span></span>

<span data-ttu-id="a70f0-118">Когда приложение отключает ведение журнала WFP (путем вызова [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), затрагиваются все приложения.</span><span class="sxs-lookup"><span data-stu-id="a70f0-118">When an application disables WFP logging (by calling [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)) all applications are affected.</span></span> <span data-ttu-id="a70f0-119">Журнал событий не очищается до тех пор, пока приложение снова не включит ведение журнала WFP, но до этого не удастся выполнить запрос к журналу событий.</span><span class="sxs-lookup"><span data-stu-id="a70f0-119">The event log is not cleaned up until an application re-enables WFP logging, but the event log cannot be queried before then.</span></span>

<span data-ttu-id="a70f0-120">Журнал событий WFP очищается после перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="a70f0-120">The WFP event log is emptied after a reboot.</span></span>

 

 




