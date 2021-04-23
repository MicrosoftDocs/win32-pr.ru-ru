---
title: Получение машинного SDO
description: Первым шагом при использовании API SDO является создание объекта компьютера SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070255"
---
# <a name="obtaining-a-machine-sdo"></a><span data-ttu-id="5e968-103">Получение машинного SDO</span><span class="sxs-lookup"><span data-stu-id="5e968-103">Obtaining a Machine SDO</span></span>

<span data-ttu-id="5e968-104">Первым шагом при использовании API SDO является создание объекта компьютера SDO.</span><span class="sxs-lookup"><span data-stu-id="5e968-104">The first step in using the SDO API is to create an SDO machine object.</span></span>

<span data-ttu-id="5e968-105">Используйте функцию [**клсидфромпрогид**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) , чтобы получить идентификатор класса (CLSID) для объекта компьютера SDO.</span><span class="sxs-lookup"><span data-stu-id="5e968-105">Use the [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) function to obtain the class identifier (CLSID) for the SDO machine object.</span></span> <span data-ttu-id="5e968-106">Программный идентификатор (ProgID), используемый для объекта, — это IAS. Сдомачине ".</span><span class="sxs-lookup"><span data-stu-id="5e968-106">The programmatic identifier (ProgID) to use for the object is "IAS.SdoMachine".</span></span>

<span data-ttu-id="5e968-107">После получения идентификатора CLSID вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с этим идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="5e968-107">Once you have the CLSID, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with this CLSID.</span></span> <span data-ttu-id="5e968-108">Укажите [**исдомачине**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) в качестве интерфейса, для которого возвращается указатель.</span><span class="sxs-lookup"><span data-stu-id="5e968-108">Specify [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) as the interface for which to return a pointer.</span></span>

<span data-ttu-id="5e968-109">Пример кода, демонстрирующий получение машинного SDO, см. [в разделе Присоединение к SDO-Enabled компьютеру](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) .</span><span class="sxs-lookup"><span data-stu-id="5e968-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to obtain a machine SDO.</span></span>

 

 