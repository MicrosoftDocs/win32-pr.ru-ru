---
description: Высокопроизводительный поставщик WMI значительно увеличивает скорость, с которой клиент WMI может получать информацию от поставщика экземпляров WMI.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Повышение эффективности работы поставщика экземпляров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fecd0d8a20a3dcccd2878996823a7eb8a7ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911503"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a><span data-ttu-id="81f5b-103">Повышение эффективности работы поставщика экземпляров</span><span class="sxs-lookup"><span data-stu-id="81f5b-103">Improving the Efficiency of an Instance Provider</span></span>

<span data-ttu-id="81f5b-104">Высокопроизводительный поставщик WMI значительно увеличивает скорость, с которой клиент WMI может получать информацию от поставщика экземпляров WMI.</span><span class="sxs-lookup"><span data-stu-id="81f5b-104">A WMI high-performance provider greatly increases the speed at which a WMI client can obtain information from a WMI instance provider.</span></span> <span data-ttu-id="81f5b-105">Основное изменение заключается в том, что высокопроизводительный поставщик работает как внутрипроцессный сервер либо на клиентское приложение, либо в инструментарий WMI.</span><span class="sxs-lookup"><span data-stu-id="81f5b-105">The main change is that a high-performance provider runs as an in-process server to either the client application or to WMI.</span></span> <span data-ttu-id="81f5b-106">Поместив поставщик в клиентский процесс, можно ускорить взаимодействие между ними.</span><span class="sxs-lookup"><span data-stu-id="81f5b-106">By placing the provider inside the client process, you can speed up the interaction between the two.</span></span>

<span data-ttu-id="81f5b-107">Дополнительные сведения о том, как предоставить поставщику экземпляров высокопроизводительный поставщик, см. в разделе [Создание поставщика экземпляров в поставщике High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="81f5b-107">For more information about how to make your instance provider a high-performance provider, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

 

 



