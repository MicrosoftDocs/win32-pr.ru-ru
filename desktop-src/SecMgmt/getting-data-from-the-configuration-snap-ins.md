---
description: 'Расширение оснастки "вложение" не позволяет напрямую запрашивать базу данных безопасности для получения информации. Вместо этого он должен запрашивать эти сведения из оснасток настройки безопасности с помощью Исцесвкаттачментдата:: GetData.'
ms.assetid: 1171beed-5b28-4f31-b33f-533e3c631b0d
title: Получение данных из оснастки конфигурации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c888cef92a354f73f01e87fca12cee2567dab48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546210"
---
# <a name="getting-data-from-the-configuration-snap-ins"></a><span data-ttu-id="41fbf-104">Получение данных из оснастки конфигурации</span><span class="sxs-lookup"><span data-stu-id="41fbf-104">Getting Data from the Configuration Snap-ins</span></span>

<span data-ttu-id="41fbf-105">Расширение оснастки "вложение" не позволяет напрямую запрашивать базу данных безопасности для получения информации.</span><span class="sxs-lookup"><span data-stu-id="41fbf-105">The attachment snap-in extension has no way to directly query the security database to retrieve information.</span></span> <span data-ttu-id="41fbf-106">Вместо этого он должен запрашивать эти сведения из оснасток настройки безопасности с помощью [**исцесвкаттачментдата:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span><span class="sxs-lookup"><span data-stu-id="41fbf-106">Instead, it must query this information from the Security Configuration snap-ins using [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span></span>

<span data-ttu-id="41fbf-107">Оснастка "вложение" может извлекать все данные при инициализации самой себя или получать информацию при открытии его узла.</span><span class="sxs-lookup"><span data-stu-id="41fbf-107">The attachment snap-in can retrieve all of the data when it initializes itself, or it can retrieve information when its node is opened.</span></span>

> [!Note]  
> <span data-ttu-id="41fbf-108">Необходимо использовать метод [**исцесвкаттачментдата:: фрибуффер**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) , чтобы освободить буфер, выделенный методом оснастки настройки безопасности [**Исцесвкаттачментдата:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span><span class="sxs-lookup"><span data-stu-id="41fbf-108">You must use the [**ISceSvcAttachmentData::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) method to free the buffer allocated by the Security Configuration snap-in method [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span></span>

 

 

 



