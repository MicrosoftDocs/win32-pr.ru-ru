---
description: '\_Класс поставщиков MSFT и классы устранения неполадок WMI представляют собой группу классов событий MSFT, связанных с событиями поставщика WMI.'
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Классы для настройки и устранения неполадок поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712107"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a><span data-ttu-id="2866a-103">Классы для настройки и устранения неполадок поставщика</span><span class="sxs-lookup"><span data-stu-id="2866a-103">Provider Configuration and Troubleshooting Classes</span></span>

<span data-ttu-id="2866a-104">Класс [**\_ поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) и классы устранения неполадок WMI представляют собой группу [классов событий MSFT](msft-classes.md) , связанных с событиями поставщика WMI.</span><span class="sxs-lookup"><span data-stu-id="2866a-104">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class and the WMI troubleshooting classes are a group of the [MSFT event classes](msft-classes.md) coupled to WMI provider events.</span></span>

<span data-ttu-id="2866a-105">Класс [**\_ поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) содержит сведения о конфигурации для поставщиков и включает следующие методы, позволяющие загружать и выгружать поставщиков, а также останавливать и возобновлять операции поставщика.</span><span class="sxs-lookup"><span data-stu-id="2866a-105">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class contains configuration information for providers and includes the following methods that allow you to load and unload providers, or suspend and resume provider operations:</span></span>

-   [<span data-ttu-id="2866a-106">**Метод Load \_ класса поставщиков MSFT**</span><span class="sxs-lookup"><span data-stu-id="2866a-106">**Load Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [<span data-ttu-id="2866a-107">**Метод Unload \_ класса поставщиков MSFT**</span><span class="sxs-lookup"><span data-stu-id="2866a-107">**UnLoad Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [<span data-ttu-id="2866a-108">**Метод Resume \_ класса поставщиков MSFT**</span><span class="sxs-lookup"><span data-stu-id="2866a-108">**Resume Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [<span data-ttu-id="2866a-109">**Метод Suspend \_ класса поставщиков MSFT**</span><span class="sxs-lookup"><span data-stu-id="2866a-109">**Suspend Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

<span data-ttu-id="2866a-110">[Классы устранения неполадок WMI](wmi-troubleshooting-classes.md) называются, чтобы указать, срабатывает ли событие до или после события поставщика.</span><span class="sxs-lookup"><span data-stu-id="2866a-110">The [WMI troubleshooting classes](wmi-troubleshooting-classes.md) are named to indicate whether the event is fired before or after a provider event.</span></span> <span data-ttu-id="2866a-111">Например, [**\_ \_ \_ Предварительный объект MSFT события AccessCheck**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) создается непосредственно перед вызовом реализации поставщика **ивбемевентсекурити:: AccessCheck**, а объект [**MSFT \_ события \_ AccessCheck \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) вызывается сразу после.</span><span class="sxs-lookup"><span data-stu-id="2866a-111">For example, the [**MSFT\_WmiProvider\_AccessCheck\_Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) object is generated immediately before calling the provider's implementation of **IWbemEventSecurity::AccessCheck**, while the [**MSFT\_WmiProvider\_AccessCheck\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) object is called immediately after.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2866a-112">См. также</span><span class="sxs-lookup"><span data-stu-id="2866a-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2866a-113">[Устранение неполадок WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="2866a-113">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="2866a-114">Классы устранения неполадок WMI</span><span class="sxs-lookup"><span data-stu-id="2866a-114">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
