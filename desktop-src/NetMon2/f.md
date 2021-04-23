---
description: Глоссарий терминов сетевой монитор, начинающихся с буквы F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 6e6b85cc-83bc-4468-b1cf-3480022a8f12
title: F (сетевой монитор)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605eb27b95526fa2f3839c06e6f259a2afec55c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673204"
---
# <a name="f-network-monitor"></a><span data-ttu-id="a523a-103">F (сетевой монитор)</span><span class="sxs-lookup"><span data-stu-id="a523a-103">F (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="a523a-104"><span id="_netmon_filter_blob_gly"></span><span id="_NETMON_FILTER_BLOB_GLY"></span>**фильтровать большой двоичный объект**</span><span class="sxs-lookup"><span data-stu-id="a523a-104"><span id="_netmon_filter_blob_gly"></span><span id="_NETMON_FILTER_BLOB_GLY"></span>**filter BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="a523a-105">Большой двоичный объект (BLOB), используемый для ограничения поиска сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="a523a-105">Binary large object (BLOB) used to restrict the search for a network interface card (NIC).</span></span> <span data-ttu-id="a523a-106">Каждая запись в объекте фильтра BLOB должна соответствовать эквивалентной записи в большом двоичном объекте поставщика сетевых пакетов (НПП), представляющем сетевую карту.</span><span class="sxs-lookup"><span data-stu-id="a523a-106">Each entry in the filter BLOB must match an equivalent entry in the network packet provider (NPP) BLOB that represents the NIC.</span></span> <span data-ttu-id="a523a-107">Например, приложение может запрашивать только карты Ethernet или карты, которые поддерживают определенную частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="a523a-107">For example, an application can request only Ethernet cards, or cards that support a specific frame rate.</span></span> <span data-ttu-id="a523a-108">Для вызова функций **жетнппблобфромуи** и **жетнппблобтабле** можно использовать большой двоичный объект фильтра.</span><span class="sxs-lookup"><span data-stu-id="a523a-108">You can use a filter BLOB to call the **GetNPPBlobFromUI** and **GetNPPBlobTable** functions.</span></span>

</dd> <dt>

<span data-ttu-id="a523a-109"><span id="_netmon_follow_set_gly"></span><span id="_NETMON_FOLLOW_SET_GLY"></span>**следовать за набором**</span><span class="sxs-lookup"><span data-stu-id="a523a-109"><span id="_netmon_follow_set_gly"></span><span id="_NETMON_FOLLOW_SET_GLY"></span>**follow set**</span></span>
</dt> <dd>

<span data-ttu-id="a523a-110">Набор протоколов, который следует за протоколом.</span><span class="sxs-lookup"><span data-stu-id="a523a-110">A protocol set that follows a protocol.</span></span> <span data-ttu-id="a523a-111">Сетевой монитор использует следующий набор протоколов, если средство синтаксического анализа не может обнаружить следующие протоколы из данных в записи.</span><span class="sxs-lookup"><span data-stu-id="a523a-111">Network Monitor uses the follow set of a protocol if the parser cannot detect the next protocol from the data in the capture.</span></span> <span data-ttu-id="a523a-112">См. также « [ *переданный набор* »](h.md)</span><span class="sxs-lookup"><span data-stu-id="a523a-112">See also [*handoff set*](h.md)</span></span>

</dd> <dt>

<span data-ttu-id="a523a-113"><span id="_netmon_frame_gly"></span><span id="_NETMON_FRAME_GLY"></span>**NOFRAMES**</span><span class="sxs-lookup"><span data-stu-id="a523a-113"><span id="_netmon_frame_gly"></span><span id="_NETMON_FRAME_GLY"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="a523a-114">Пакет данных, передаваемый в виде одной единицы по сети.</span><span class="sxs-lookup"><span data-stu-id="a523a-114">A packet of data that is transmitted as one unit over a network.</span></span> <span data-ttu-id="a523a-115">Каждый кадр соответствует одной базовой организации и содержит управляющую информацию, например синхронизацию символов, адреса станции, значение проверки ошибок и переменный объем данных.</span><span class="sxs-lookup"><span data-stu-id="a523a-115">Each frame follows the same basic organization, and contains control information such as synchronizing characters, station addresses, an error-checking value, and a variable amount of data.</span></span> <span data-ttu-id="a523a-116">Также называется пакетом.</span><span class="sxs-lookup"><span data-stu-id="a523a-116">Also called a packet.</span></span>

</dd> <dt>

<span data-ttu-id="a523a-117"><span id="_netmon_frame_viewer_window_gly"></span><span id="_NETMON_FRAME_VIEWER_WINDOW_GLY"></span>**окно средства просмотра кадров**</span><span class="sxs-lookup"><span data-stu-id="a523a-117"><span id="_netmon_frame_viewer_window_gly"></span><span id="_NETMON_FRAME_VIEWER_WINDOW_GLY"></span>**frame viewer window**</span></span>
</dt> <dd>

<span data-ttu-id="a523a-118">Сетевой монитор окно, в котором отображаются подробные сведения об отдельных кадрах.</span><span class="sxs-lookup"><span data-stu-id="a523a-118">A Network Monitor window that displays detailed information about individual frames.</span></span> <span data-ttu-id="a523a-119">Можно открыть несколько окон средства просмотра кадров за один раз.</span><span class="sxs-lookup"><span data-stu-id="a523a-119">You can open several frame viewer windows at one time.</span></span>

</dd> </dl>

 

 



