---
description: Чтобы настроить экспертов, используйте пользовательские диалоговые окна и функцию configure.
ms.assetid: 6298fa7b-ddc8-4924-9616-6eed67ec48db
title: Настройка экспертов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152d728de1dc5a40836a9a2cc2c822a389e3f973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565011"
---
# <a name="configuring-experts"></a><span data-ttu-id="2cef0-103">Настройка экспертов</span><span class="sxs-lookup"><span data-stu-id="2cef0-103">Configuring Experts</span></span>

<span data-ttu-id="2cef0-104">Чтобы настроить экспертов, используйте пользовательские диалоговые окна и функцию [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="2cef0-104">To configure experts, use the custom dialog boxes and the [**Configure**](configure.md) function.</span></span> <span data-ttu-id="2cef0-105">При написании экспертов по сетевым мониторам вы можете выбрать один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="2cef0-105">When you write Network monitor experts, you have a choice.</span></span> <span data-ttu-id="2cef0-106">Можно создать набор элементов конфигурации по умолчанию, которые можно использовать при первоначальном запуске эксперта, или разрешить сетевой монитор пользователям настраивать эксперт во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2cef0-106">You can create a set of default configuration items that can be used when the expert initially runs, or you can allow Network Monitor users to configure the expert at run time.</span></span> <span data-ttu-id="2cef0-107">Конфигурации для каждого эксперта хранятся сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="2cef0-107">Configurations for each expert are stored by Network Monitor.</span></span> <span data-ttu-id="2cef0-108">В качестве параметра пользователи могут сбросить настройки эксперта к исходным параметрам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2cef0-108">As an option, users can reset the expert configuration back to original default settings.</span></span> <span data-ttu-id="2cef0-109">Имейте в виду, что можно обойти использование **настройки** , разработав эксперта, который передает фиксированную конфигурацию для сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="2cef0-109">Be aware that you can bypass the use of **Configure** by developing an expert that passes a fixed configuration to Network Monitor.</span></span>

![диалоговое окно "Конфигурация експер"](images/dialog.png)

 

 



