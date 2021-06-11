---
title: Использование расширений NPS
description: Узнайте об использовании расширений NPS. Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Служба проверки подлинности в Интернете, задачи
- Служба проверки подлинности в Интернете, использование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f422c005d6810a4035450e24de1324b28361f1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989075"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="a7ea7-106">Использование расширений NPS</span><span class="sxs-lookup"><span data-stu-id="a7ea7-106">Using NPS Extensions</span></span>

<span data-ttu-id="a7ea7-107">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS).</span><span class="sxs-lookup"><span data-stu-id="a7ea7-107">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="a7ea7-108">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="a7ea7-108">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="a7ea7-109">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="a7ea7-109">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="a7ea7-110">\* \* Windows Server 2008 R2 и Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="a7ea7-110">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="a7ea7-111">Примеры набора номера и Мапнаме расширяют функциональные возможности NPS.</span><span class="sxs-lookup"><span data-stu-id="a7ea7-111">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="a7ea7-112">Образец</span><span class="sxs-lookup"><span data-stu-id="a7ea7-112">Sample</span></span>             | <span data-ttu-id="a7ea7-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a7ea7-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ea7-114">Набор номера</span><span class="sxs-lookup"><span data-stu-id="a7ea7-114">DialIn</span></span><br/>  | <span data-ttu-id="a7ea7-115">В этом примере реализуется библиотека DLL расширения RADIUS, которая проверяет бит коммутируемого подключения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7ea7-115">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="a7ea7-116">мапнаме</span><span class="sxs-lookup"><span data-stu-id="a7ea7-116">MapName</span></span><br/> | <span data-ttu-id="a7ea7-117">Этот пример библиотеки DLL расширения выполняет поиск всех доверенных доменов для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a7ea7-117">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="a7ea7-118">Это позволяет пользователям из нескольких доменов проходить проверку подлинности без указания имени домена.</span><span class="sxs-lookup"><span data-stu-id="a7ea7-118">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="a7ea7-119">Исходный код для примеров приложений Мапнаме и Dialin можно найти в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="a7ea7-119">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="a7ea7-120">*Расположение*,% путь установки%, обозначает базовый каталог установки для компьютеров с архитектурой x64.</span><span class="sxs-lookup"><span data-stu-id="a7ea7-120">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="a7ea7-121">См. также пакет средств [разработки программного обеспечения Windows (SDK) для Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), пакет средств разработки программного обеспечения Microsoft Windows (SDK) и [Загружаемые файлы для разработки приложений для Магазина Windows](https://msdn.microsoft.com/windows/apps/br229516).</span><span class="sxs-lookup"><span data-stu-id="a7ea7-121">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="a7ea7-122">Windows SDK для Windows 8</span><span class="sxs-lookup"><span data-stu-id="a7ea7-122">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="a7ea7-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7ea7-123">Windows Server 2012</span></span>

<span data-ttu-id="a7ea7-124">Ссылка для скачивания: н/д</span><span class="sxs-lookup"><span data-stu-id="a7ea7-124">Download link: N/A</span></span>

<span data-ttu-id="a7ea7-125">Мапнаме: нет</span><span class="sxs-lookup"><span data-stu-id="a7ea7-125">MapName: No</span></span>

<span data-ttu-id="a7ea7-126">Набор номера: нет</span><span class="sxs-lookup"><span data-stu-id="a7ea7-126">DialIn: No</span></span>

<span data-ttu-id="a7ea7-127">Расположение: н/д</span><span class="sxs-lookup"><span data-stu-id="a7ea7-127">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="a7ea7-128">Пакет средств разработки программного обеспечения Microsoft Windows (SDK) для Windows 7 и платформа .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="a7ea7-128">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="a7ea7-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7ea7-129">Windows Server 2008 R2</span></span>

<span data-ttu-id="a7ea7-130">Ссылка для скачивания: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="a7ea7-130">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="a7ea7-131">Мапнаме: Да</span><span class="sxs-lookup"><span data-stu-id="a7ea7-131">MapName: Yes</span></span>

<span data-ttu-id="a7ea7-132">Набор номера: нет</span><span class="sxs-lookup"><span data-stu-id="a7ea7-132">DialIn: No</span></span>

<span data-ttu-id="a7ea7-133">Расположение:% путь установки% \\ пакеты SDK Microsoft \\ Windows \\ v 7.1 \\ примеры \\ нетдс \\ IAS</span><span class="sxs-lookup"><span data-stu-id="a7ea7-133">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="a7ea7-134">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a7ea7-134">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="a7ea7-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7ea7-135">Windows Server 2008</span></span>

<span data-ttu-id="a7ea7-136">Ссылка для скачивания: <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="a7ea7-136">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="a7ea7-137">Мапнаме: Да</span><span class="sxs-lookup"><span data-stu-id="a7ea7-137">MapName: Yes</span></span>

<span data-ttu-id="a7ea7-138">Набор номера: нет</span><span class="sxs-lookup"><span data-stu-id="a7ea7-138">DialIn: No</span></span>

<span data-ttu-id="a7ea7-139">Расположение:% путь установки% \\ пакеты SDK Microsoft \\ Windows \\ v 6.1 \\ примеры \\ нетдс \\ IAS</span><span class="sxs-lookup"><span data-stu-id="a7ea7-139">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a7ea7-140">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a7ea7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7ea7-141">Загружаемые файлы для разработчиков</span><span class="sxs-lookup"><span data-stu-id="a7ea7-141">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="a7ea7-142">Windows SDK для Windows 8</span><span class="sxs-lookup"><span data-stu-id="a7ea7-142">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





