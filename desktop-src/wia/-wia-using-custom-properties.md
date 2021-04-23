---
description: Использование пользовательских свойств.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Использование пользовательских свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692410"
---
# <a name="using-custom-properties"></a><span data-ttu-id="d3449-103">Использование пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="d3449-103">Using Custom Properties</span></span>

<span data-ttu-id="d3449-104">**Использование пользовательских свойств**.</span><span class="sxs-lookup"><span data-stu-id="d3449-104">**Using Custom Properties**.</span></span>

<span data-ttu-id="d3449-105">Драйвер для получения образа Windows (WIA) может определять собственные пользовательские свойства.</span><span class="sxs-lookup"><span data-stu-id="d3449-105">A Windows Image Acquisition (WIA) driver can define its own custom properties.</span></span> <span data-ttu-id="d3449-106">Вызывающие объекты могут манипулировать пользовательскими свойствами точно так же, как обычные свойства WIA.</span><span class="sxs-lookup"><span data-stu-id="d3449-106">Callers can manipulate custom properties just as they would normal WIA properties.</span></span> <span data-ttu-id="d3449-107">Однако доступ к этим пользовательским свойствам могут получить только приложение или пользовательский модуль пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d3449-107">However, only your application or custom UI module can access these custom properties.</span></span>

<span data-ttu-id="d3449-108">Драйверы WIA должны определять пользовательские свойства, чтобы иметь идентификаторы свойств, которые смещены с помощью WIA \_ Private \_ девпроп для свойств устройства, и использовать \_ закрытый \_ итемпроп WIA для обычных свойств элемента, например внутри [ивиаминидрв::d рвинититемпропертиес](https://msdn.microsoft.com/library/ms794131.aspx).</span><span class="sxs-lookup"><span data-stu-id="d3449-108">WIA drivers should define the custom properties to have property identifiers that are offset by WIA\_PRIVATE\_DEVPROP for device properties, and use WIA\_PRIVATE\_ITEMPROP for normal item properties, such as inside [IWiaMiniDrv::drvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx).</span></span> <span data-ttu-id="d3449-109">Дополнительные сведения см. в разделе [Определение пользовательских свойств](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d3449-109">For more information, see [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="d3449-110">Существует два способа передачи пользовательских параметров драйверам WIA.</span><span class="sxs-lookup"><span data-stu-id="d3449-110">There are two ways to pass custom parameters to WIA drivers.</span></span>

<span data-ttu-id="d3449-111">Первый вариант — использовать метод **ивиаитемекстрас:: Escape** (описанный в документации по Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="d3449-111">The first option is to use the **IWiaItemExtras::Escape** method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="d3449-112">Это похоже на метод [истиусд:: Escape](https://msdn.microsoft.com/library/ms794396.aspx) , но позволяет вызывающим объектам напрямую использовать WIA, вместо того чтобы использовать методы сти.</span><span class="sxs-lookup"><span data-stu-id="d3449-112">This is similar to the [IStiUSD::Escape](https://msdn.microsoft.com/library/ms794396.aspx) method, but it allows callers to use WIA directly, instead of using STI methods.</span></span> <span data-ttu-id="d3449-113">С помощью **ивиаитемекстрас:: Escape** можно передать любые сведения в драйвер, и драйвер может передать любую информацию.</span><span class="sxs-lookup"><span data-stu-id="d3449-113">Using **IWiaItemExtras::Escape**, you can pass any information to the driver, and the driver can pass any information back.</span></span> <span data-ttu-id="d3449-114">Служба WIA управляет только теми буферами, которые передаются между вызывающим и драйвером.</span><span class="sxs-lookup"><span data-stu-id="d3449-114">The WIA service manages only those buffers passed between the caller and the driver.</span></span>

<span data-ttu-id="d3449-115">Второй вариант — использовать пользовательские свойства.</span><span class="sxs-lookup"><span data-stu-id="d3449-115">The second option is to use custom properties.</span></span> <span data-ttu-id="d3449-116">Использование метода **ивиаитемекстрас:: Escape** является более гибким, чем использование настраиваемых свойств WIA, но пользовательские свойства WIA позволяют хранить информацию в потоке свойств элемента, чтобы драйвер мог считывать информацию в другое время.</span><span class="sxs-lookup"><span data-stu-id="d3449-116">Using the **IWiaItemExtras::Escape** method is more flexible than using custom WIA properties, but custom WIA properties allow you to store information in the item's property stream so that the driver can read the information at another time.</span></span>

 

 



