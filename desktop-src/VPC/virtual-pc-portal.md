---
title: Windows Virtual PC
description: Использование COM-интерфейсов Windows Virtual PC для создания виртуальной машины и установки виртуальной машины; Windows Virtual PC — это новейшая технология виртуализации Майкрософт.
ms.assetid: d47eee76-059b-43dc-a51f-7c08d932a1c7
keywords:
- Виртуальный ПК Windows Virtual PC
- Виртуальный ПК Windows Virtual PC, Домашняя страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9dbe0d05100876ae54d327d1fe7ac8cb53d40c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691535"
---
# <a name="windows-virtual-pc"></a><span data-ttu-id="2cc7b-105">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2cc7b-105">Windows Virtual PC</span></span>

<span data-ttu-id="2cc7b-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2cc7b-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2cc7b-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](../hyperv_v2/windows-virtualization-portal.md).\]</span><span class="sxs-lookup"><span data-stu-id="2cc7b-107">Instead, use the [Hyper-V WMI provider (V2)](../hyperv_v2/windows-virtualization-portal.md).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="2cc7b-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="2cc7b-108">Purpose</span></span>

<span data-ttu-id="2cc7b-109">В этой документации содержатся сведения о COM-интерфейсе Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="2cc7b-109">This documentation provides information about the Windows Virtual PC COM interface.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="2cc7b-110">Где применимо</span><span class="sxs-lookup"><span data-stu-id="2cc7b-110">Where applicable</span></span>

<span data-ttu-id="2cc7b-111">Windows Virtual PC — это новейшая технология виртуализации Майкрософт; Она позволяет запускать множество приложений для повышения производительности в виртуальной среде Windows с одним щелчком непосредственно из Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2cc7b-111">Windows Virtual PC is the latest Microsoft virtualization technology; it enables you to run many productivity applications on a virtual Windows environment, with a single click, directly from Windows 7.</span></span> <span data-ttu-id="2cc7b-112">Вы можете создать отдельные виртуальные машины поверх рабочего стола Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2cc7b-112">You can create separate virtual machines on top of your Windows 7 desktop.</span></span> <span data-ttu-id="2cc7b-113">Каждая виртуальная машина эмулирует полную аппаратную систему — от процессора до сетевой карты — в автономной изолированной программной среде, обеспечивая одновременную работу несовместимых систем.</span><span class="sxs-lookup"><span data-stu-id="2cc7b-113">Each virtual machine emulates a complete hardware system—from processor to network card—in a self-contained, isolated software environment, enabling the simultaneous operation of otherwise incompatible systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2cc7b-114">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="2cc7b-114">Developer audience</span></span>

<span data-ttu-id="2cc7b-115">COM-интерфейсы виртуальных ПК Windows предназначены для разработчиков, создающих клиентские приложения, автоматизирующие развертывание и эксплуатацию виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2cc7b-115">The Windows Virtual PC COM interfaces are for developers who are creating client applications that automate the deployment and operation of virtual machines.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2cc7b-116">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="2cc7b-116">Run-time requirements</span></span>

<span data-ttu-id="2cc7b-117">Для Windows Virtual PC требуется одна из следующих выпусков Windows 7: Домашняя базовая, Домашняя расширенная, профессиональная, максимальная или Корпоративная.</span><span class="sxs-lookup"><span data-stu-id="2cc7b-117">Windows Virtual PC requires one of the following Windows 7 editions - Home Basic, Home Premium, Professional, Ultimate, or Enterprise edition.</span></span>

<span data-ttu-id="2cc7b-118">Чтобы получить связанные файлы заголовка и библиотеки, установите Windows SDK для Windows 7 из [центра загрузки Майкрософт](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="2cc7b-118">To obtain the related header and library files, install the Windows SDK for Windows 7 from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2cc7b-119">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="2cc7b-119">In this section</span></span>

-   [<span data-ttu-id="2cc7b-120">Справочник по виртуальным ПК Windows</span><span class="sxs-lookup"><span data-stu-id="2cc7b-120">Windows Virtual PC Reference</span></span>](virtual-pc-reference.md)

## <a name="related-topics"></a><span data-ttu-id="2cc7b-121">См. также</span><span class="sxs-lookup"><span data-stu-id="2cc7b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cc7b-122">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2cc7b-122">Windows Virtual PC</span></span>](https://www.microsoft.com/windows/virtual-pc/)
</dt> </dl>

 

 