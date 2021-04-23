---
title: Лицензии
description: Лицензии
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Windows Media Format SDK, лицензии DRM
- Пакет SDK для Windows Media Format, лицензии для DRM
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Управление цифровыми правами (DRM), лицензирование защищенных файлов
- DRM (Управление цифровыми правами), лицензирование защищенных файлов
- лицензии, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332307"
---
# <a name="licenses"></a><span data-ttu-id="cdcea-111">Лицензии</span><span class="sxs-lookup"><span data-stu-id="cdcea-111">Licenses</span></span>

<span data-ttu-id="cdcea-112">Лицензия — это набор данных, описывающих условия, при которых данные в защищенных файлах могут быть прочитаны.</span><span class="sxs-lookup"><span data-stu-id="cdcea-112">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="cdcea-113">Каждая лицензия применяется к идентификатору ключа, который обычно назначается одному файлу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cdcea-113">Each license applies to a key identifier, which is typically assigned to a single media file.</span></span> <span data-ttu-id="cdcea-114">Этот идентификатор используется для идентификации защищенного содержимого в лицензии.</span><span class="sxs-lookup"><span data-stu-id="cdcea-114">This identifier is what is used to identify the protected content in the license.</span></span>

<span data-ttu-id="cdcea-115">Каждая лицензия указывает одно или несколько действий, которые могут быть выполнены с защищенным содержимым.</span><span class="sxs-lookup"><span data-stu-id="cdcea-115">Each license specifies one or more actions that can be performed with the protected content.</span></span> <span data-ttu-id="cdcea-116">Эти действия, также называемые правами, могут быть ограничены несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="cdcea-116">These actions, also called rights, can be limited in a number of ways.</span></span> <span data-ttu-id="cdcea-117">Объединяя даты начала, даты окончания, количества и ограничения по времени, издатель лицензии может создавать почти любое мнимое ограничение справа.</span><span class="sxs-lookup"><span data-stu-id="cdcea-117">By combining start dates, end dates, counts, and time limits, the license issuer can create almost any imaginable limitation on a right.</span></span>

<span data-ttu-id="cdcea-118">Лицензии выдаются веб-службой.</span><span class="sxs-lookup"><span data-stu-id="cdcea-118">Licenses are issued by a Web service.</span></span> <span data-ttu-id="cdcea-119">При получении лицензии она хранится на клиентском компьютере в локальном хранилище лицензий, которое является защищенным файлом, который содержит лицензии и другие данные DRM.</span><span class="sxs-lookup"><span data-stu-id="cdcea-119">When a license is acquired, it is stored on the client computer in the local license store, which is a protected file that contains licenses and other DRM data.</span></span> <span data-ttu-id="cdcea-120">Если доступ к защищенному содержимому осуществляется приложением, подсистема DRM ищет в локальном хранилище лицензий лицензию, которая предоставляет соответствующее право.</span><span class="sxs-lookup"><span data-stu-id="cdcea-120">When protected content is accessed by an application, the DRM subsystem searches the local license store for a license that grants the appropriate right.</span></span> <span data-ttu-id="cdcea-121">Если лицензия не найдена, приложение может получить его на основе информации, хранящейся в заголовке DRM файла.</span><span class="sxs-lookup"><span data-stu-id="cdcea-121">If no license is found, the application can acquire one based on information stored in the DRM header of the file.</span></span>

<span data-ttu-id="cdcea-122">Для одного и того же защищенного файла может быть выдана несколько лицензий.</span><span class="sxs-lookup"><span data-stu-id="cdcea-122">Multiple licenses can be issued for the same protected file.</span></span> <span data-ttu-id="cdcea-123">Если подсистема DRM определяет, разрешено ли действие, она объединяет права всех лицензий, которые применяются.</span><span class="sxs-lookup"><span data-stu-id="cdcea-123">When the DRM subsystem determines whether an action is allowed, it aggregates the rights from all licenses that apply.</span></span> <span data-ttu-id="cdcea-124">Каждой лицензии можно назначить приоритет.</span><span class="sxs-lookup"><span data-stu-id="cdcea-124">Each license can be assigned a priority.</span></span> <span data-ttu-id="cdcea-125">Если к действию применяется более одной лицензии, проверяется лицензия с наивысшим приоритетом, чтобы определить, нужно ли уменьшать количество счетчиков.</span><span class="sxs-lookup"><span data-stu-id="cdcea-125">If more than one license applies to an action, the highest priority license is checked to determine whether counts need to be decremented.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdcea-126">См. также</span><span class="sxs-lookup"><span data-stu-id="cdcea-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdcea-127">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="cdcea-127">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




