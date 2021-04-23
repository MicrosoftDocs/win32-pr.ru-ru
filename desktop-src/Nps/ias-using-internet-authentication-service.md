---
title: Использование расширений NPS
description: Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Служба проверки подлинности в Интернете, задачи
- Служба проверки подлинности в Интернете, использование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104533065"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="525aa-105">Использование расширений NPS</span><span class="sxs-lookup"><span data-stu-id="525aa-105">Using NPS Extensions</span></span>

<span data-ttu-id="525aa-106">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS).</span><span class="sxs-lookup"><span data-stu-id="525aa-106">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="525aa-107">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="525aa-107">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="525aa-108">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="525aa-108">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="525aa-109">\* \* Windows Server 2008 R2 и Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="525aa-109">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="525aa-110">Примеры набора номера и Мапнаме расширяют функциональные возможности NPS.</span><span class="sxs-lookup"><span data-stu-id="525aa-110">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="525aa-111">Образец</span><span class="sxs-lookup"><span data-stu-id="525aa-111">Sample</span></span>             | <span data-ttu-id="525aa-112">Описание</span><span class="sxs-lookup"><span data-stu-id="525aa-112">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="525aa-113">Набор номера</span><span class="sxs-lookup"><span data-stu-id="525aa-113">DialIn</span></span><br/>  | <span data-ttu-id="525aa-114">В этом примере реализуется библиотека DLL расширения RADIUS, которая проверяет бит коммутируемого подключения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="525aa-114">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="525aa-115">мапнаме</span><span class="sxs-lookup"><span data-stu-id="525aa-115">MapName</span></span><br/> | <span data-ttu-id="525aa-116">Этот пример библиотеки DLL расширения выполняет поиск всех доверенных доменов для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="525aa-116">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="525aa-117">Это позволяет пользователям из нескольких доменов проходить проверку подлинности без указания имени домена.</span><span class="sxs-lookup"><span data-stu-id="525aa-117">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="525aa-118">Исходный код для примеров приложений Мапнаме и Dialin можно найти в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="525aa-118">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="525aa-119">*Расположение*,% путь установки%, обозначает базовый каталог установки для компьютеров с архитектурой x64.</span><span class="sxs-lookup"><span data-stu-id="525aa-119">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="525aa-120">См. также пакет средств [разработки программного обеспечения Windows (SDK) для Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), пакет средств разработки программного обеспечения Microsoft Windows (SDK) и [Загружаемые файлы для разработки приложений для Магазина Windows](https://msdn.microsoft.com/windows/apps/br229516).</span><span class="sxs-lookup"><span data-stu-id="525aa-120">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="525aa-121">Windows SDK для Windows 8</span><span class="sxs-lookup"><span data-stu-id="525aa-121">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="525aa-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="525aa-122">Windows Server 2012</span></span>

<span data-ttu-id="525aa-123">Ссылка для скачивания: н/д</span><span class="sxs-lookup"><span data-stu-id="525aa-123">Download link: N/A</span></span>

<span data-ttu-id="525aa-124">Мапнаме: нет</span><span class="sxs-lookup"><span data-stu-id="525aa-124">MapName: No</span></span>

<span data-ttu-id="525aa-125">Набор номера: нет</span><span class="sxs-lookup"><span data-stu-id="525aa-125">DialIn: No</span></span>

<span data-ttu-id="525aa-126">Расположение: н/д</span><span class="sxs-lookup"><span data-stu-id="525aa-126">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="525aa-127">Пакет средств разработки программного обеспечения Microsoft Windows (SDK) для Windows 7 и платформа .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="525aa-127">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="525aa-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="525aa-128">Windows Server 2008 R2</span></span>

<span data-ttu-id="525aa-129">Ссылка для скачивания: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="525aa-129">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="525aa-130">Мапнаме: Да</span><span class="sxs-lookup"><span data-stu-id="525aa-130">MapName: Yes</span></span>

<span data-ttu-id="525aa-131">Набор номера: нет</span><span class="sxs-lookup"><span data-stu-id="525aa-131">DialIn: No</span></span>

<span data-ttu-id="525aa-132">Расположение:% путь установки% \\ пакеты SDK Microsoft \\ Windows \\ v 7.1 \\ примеры \\ нетдс \\ IAS</span><span class="sxs-lookup"><span data-stu-id="525aa-132">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="525aa-133">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="525aa-133">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="525aa-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="525aa-134">Windows Server 2008</span></span>

<span data-ttu-id="525aa-135">Ссылка для скачивания: <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="525aa-135">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="525aa-136">Мапнаме: Да</span><span class="sxs-lookup"><span data-stu-id="525aa-136">MapName: Yes</span></span>

<span data-ttu-id="525aa-137">Набор номера: нет</span><span class="sxs-lookup"><span data-stu-id="525aa-137">DialIn: No</span></span>

<span data-ttu-id="525aa-138">Расположение:% путь установки% \\ пакеты SDK Microsoft \\ Windows \\ v 6.1 \\ примеры \\ нетдс \\ IAS</span><span class="sxs-lookup"><span data-stu-id="525aa-138">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="525aa-139">См. также</span><span class="sxs-lookup"><span data-stu-id="525aa-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="525aa-140">Загружаемые файлы для разработчиков</span><span class="sxs-lookup"><span data-stu-id="525aa-140">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="525aa-141">Windows SDK для Windows 8</span><span class="sxs-lookup"><span data-stu-id="525aa-141">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





