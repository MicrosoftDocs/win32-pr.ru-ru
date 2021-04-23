---
description: Чтобы максимально упростить реализацию драйвера, служба "получение образа Windows" (WIA) предоставляет библиотеку Минидривер Service Library, которая выполняет многие административные задачи, необходимые для архитектуры WIA.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Библиотека WIA Минидривер Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45856fb795810e4e447a226f1b92a28698f08cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692403"
---
# <a name="wia-minidriver-service-library"></a><span data-ttu-id="eec61-103">Библиотека WIA Минидривер Service</span><span class="sxs-lookup"><span data-stu-id="eec61-103">WIA Minidriver Service Library</span></span>

<span data-ttu-id="eec61-104">Чтобы максимально упростить реализацию драйвера, служба "получение образа Windows" (WIA) предоставляет библиотеку Минидривер Service Library, которая выполняет многие административные задачи, необходимые для архитектуры WIA.</span><span class="sxs-lookup"><span data-stu-id="eec61-104">To simplify driver implementation as much as possible, Windows Image Acquisition (WIA) provides a Minidriver Service Library that performs many of the administrative tasks required by the WIA architecture.</span></span> <span data-ttu-id="eec61-105">Библиотека служб предоставляет вспомогательные функции для обслуживания дерева объектов [интерфейса ивиадрвитем](https://msdn.microsoft.com/library/ms793976.aspx) устройства.</span><span class="sxs-lookup"><span data-stu-id="eec61-105">The service library provides helper functions to maintain the device's tree of [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) objects.</span></span>

<span data-ttu-id="eec61-106">Основные функции библиотеки службы выполняют вспомогательные функции, которые в противном случае должны быть реализованы большинством драйверов устройств.</span><span class="sxs-lookup"><span data-stu-id="eec61-106">The basic service library functions perform helper functions that most device drivers would otherwise need to implement.</span></span> <span data-ttu-id="eec61-107">Эти функции считывают и записывают свойства.</span><span class="sxs-lookup"><span data-stu-id="eec61-107">These functions read and write properties.</span></span> <span data-ttu-id="eec61-108">Они также создают объекты элементов драйвера и копируют свойства сведений об устройстве.</span><span class="sxs-lookup"><span data-stu-id="eec61-108">They also create driver item objects and copy device information properties.</span></span>

 

 



