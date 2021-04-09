---
title: Настройка начального Интернет-магазина
description: Настройка начального Интернет-магазина
ms.assetid: 86d98936-8f20-4395-be5f-37800162aa89
keywords:
- Интернет-магазины проигрывателя Windows Media, Установка начальных Интернет-магазинов
- Интернет-магазины, Настройка начальных Интернет-магазинов
- Тип 1 Интернет-магазины, Настройка начальных Интернет-магазинов
- Тип 2 Интернет-магазинов, Настройка начальных Интернет-магазинов
- Интернет-магазины проигрывателя Windows Media, первое просматриваемое онлайн-хранилище
- Интернет-магазины, первое просматриваемое интерактивное хранилище
- Тип 1 Интернет-магазины, первое просматриваемое онлайн-хранилище
- Тип 2 Интернет-магазинов, первое просматриваемое онлайн-хранилище
- Первое просмотренное Интернет-хранилище
- Настройка начальных Интернет-магазинов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fff7dc9b2df43f4b18c257b9b9c36998cbc1334
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888828"
---
# <a name="setting-the-initial-online-store"></a><span data-ttu-id="8605e-113">Настройка начального Интернет-магазина</span><span class="sxs-lookup"><span data-stu-id="8605e-113">Setting the Initial Online Store</span></span>

<span data-ttu-id="8605e-114">Дополнительные сведения о распространении программного обеспечения проигрывателя Windows Media с помощью приложения см. в разделе [распространение программного обеспечения проигрывателя Windows Media](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="8605e-114">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="8605e-115">Когда пользователь впервые устанавливает проигрыватель Windows Media, приложение установки устанавливает для первоначального активного интернет-магазина значение по умолчанию, выбранное корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="8605e-115">When a user first installs Windows Media Player, the setup application sets the initial active online store to a default chosen by Microsoft.</span></span> <span data-ttu-id="8605e-116">Изготовитель персональных компьютеров может изменить этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8605e-116">Personal computer original equipment manufacturers (OEMs) can choose to change this setting.</span></span>

<span data-ttu-id="8605e-117">Чтобы указать и настроить первое интерактивное хранилище, которое видит пользователь при установке проигрывателя Windows Media, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8605e-117">To specify and configure the first online store that the user sees when he or she installs Windows Media Player, you must:</span></span>

-   <span data-ttu-id="8605e-118">Создайте документ ServiceInfo, который будет установлен на жестком диске пользователя.</span><span class="sxs-lookup"><span data-stu-id="8605e-118">Create a ServiceInfo document that you install on the user's hard disk.</span></span> <span data-ttu-id="8605e-119">Этот документ содержит сведения о настройке начального активного интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="8605e-119">This document contains the information about how to configure the initial active online store.</span></span>
-   <span data-ttu-id="8605e-120">Добавьте набор параметров командной строки при запуске приложения установки.</span><span class="sxs-lookup"><span data-stu-id="8605e-120">Append a set of command-line parameters when running the setup application.</span></span>

<span data-ttu-id="8605e-121">Существует три сценария установки проигрывателя Windows Media и настройки первоначального Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="8605e-121">There are three scenarios for installing Windows Media Player and setting the initial online store.</span></span> <span data-ttu-id="8605e-122">В следующих разделах приводятся дополнительные сведения о каждом сценарии.</span><span class="sxs-lookup"><span data-stu-id="8605e-122">The following sections provide more details about each scenario:</span></span>

-   [<span data-ttu-id="8605e-123">Установка в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="8605e-123">Installing While Offline</span></span>](installing-while-offline.md)
-   [<span data-ttu-id="8605e-124">Установка с компакт-диска в режиме «в сети»</span><span class="sxs-lookup"><span data-stu-id="8605e-124">Installing from a CD While Online</span></span>](installing-from-a-cd-while-online.md)
-   [<span data-ttu-id="8605e-125">Установка из Интернета в режиме «в сети»</span><span class="sxs-lookup"><span data-stu-id="8605e-125">Installing from the Web While Online</span></span>](installing-from-the-web-while-online.md)

## <a name="related-topics"></a><span data-ttu-id="8605e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8605e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8605e-127">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="8605e-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8605e-128">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="8605e-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="8605e-129">**Параметры командной строки программы установки для Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="8605e-129">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




