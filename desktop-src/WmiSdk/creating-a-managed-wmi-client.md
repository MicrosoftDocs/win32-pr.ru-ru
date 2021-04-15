---
description: Инструментарий WMI в настоящее время не поддерживает управляемый код на WMI, но поддерживается в MI.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Создание управляемого клиента WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702080"
---
# <a name="creating-a-managed-wmi-client"></a><span data-ttu-id="870aa-103">Создание управляемого клиента WMI</span><span class="sxs-lookup"><span data-stu-id="870aa-103">Creating a Managed WMI Client</span></span>

<span data-ttu-id="870aa-104">Текущий выпуск WMI содержит пространство имен System. Management, которое предоставляет ряд API, взаимодействующих с WMI.</span><span class="sxs-lookup"><span data-stu-id="870aa-104">The current release of WMI does contain the System.Management namespace, which exposes a number of API's that interact with WMI.</span></span> <span data-ttu-id="870aa-105">Однако использовать это пространство имен не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="870aa-105">However, it is not recommended that you use this namespace.</span></span>

<span data-ttu-id="870aa-106">Если вы хотите создать управляемый клиент WMI, рекомендуется использовать инфраструктуру управления Windows (MI).</span><span class="sxs-lookup"><span data-stu-id="870aa-106">If you wish to create a managed WMI client, it is recommended that you use the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="870aa-107">MI — это версия WMI следующего поколения, которая содержит полную поддержку управляемого кода.</span><span class="sxs-lookup"><span data-stu-id="870aa-107">MI is the next-generation version of WMI, and contains full support for managed code.</span></span> <span data-ttu-id="870aa-108">Дополнительные сведения см. [в разделе Реализация управляемого клиента MI](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).</span><span class="sxs-lookup"><span data-stu-id="870aa-108">For more information, see [How to Implement a Managed MI Client](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).</span></span>

 

 
