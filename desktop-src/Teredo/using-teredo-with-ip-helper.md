---
title: Использование Teredo с вспомогательным модулем IP
description: API вспомогательного приложения протокола Интернета (IP-адрес) используется приложением для сбора и предоставления важной информации о конфигурации сети локального компьютера.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792510"
---
# <a name="using-teredo-with-ip-helper"></a><span data-ttu-id="0ac38-103">Использование Teredo с вспомогательным модулем IP</span><span class="sxs-lookup"><span data-stu-id="0ac38-103">Using Teredo with IP Helper</span></span>

<span data-ttu-id="0ac38-104">API [вспомогательного приложения протокола Интернета](/windows/desktop/IpHlp/about-ip-helper) (IP-адрес) используется приложением для сбора и предоставления важной информации о конфигурации сети локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="0ac38-104">The [Internet Protocol Helper](/windows/desktop/IpHlp/about-ip-helper) (IP Helper) API is utilized by an application to gather and provide important information regarding the networking configuration of the local machine.</span></span> <span data-ttu-id="0ac38-105">При работе на платформе Windows Vista эта информация включает в себя динамический UDP-порт, назначенный интерфейсу Teredo, и изменения, которые могут возникать в назначенный порт.</span><span class="sxs-lookup"><span data-stu-id="0ac38-105">When operating on the Windows Vista platform, this information includes the dynamic UDP port assigned to the Teredo interface and changes that may occur to the designated port.</span></span>

<span data-ttu-id="0ac38-106">Для упрощения использования интерфейса Teredo используются следующие функции API вспомогательного приложения IP:</span><span class="sxs-lookup"><span data-stu-id="0ac38-106">The following functions are utilized by the IP Helper API to facilitate the use of the Teredo interface:</span></span>

-   [<span data-ttu-id="0ac38-107">**жеттередопорт**</span><span class="sxs-lookup"><span data-stu-id="0ac38-107">**GetTeredoPort**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="0ac38-108">**нотифитередопортчанже**</span><span class="sxs-lookup"><span data-stu-id="0ac38-108">**NotifyTeredoPortChange**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="0ac38-109">**нотифистаблеуникастипаддресстабле**</span><span class="sxs-lookup"><span data-stu-id="0ac38-109">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 