---
description: Поставщики WMI обычно предназначены для предоставления сведений об определенном управляемом объекте на одном компьютере.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Совместное связывание классов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693550"
---
# <a name="linking-classes-together"></a><span data-ttu-id="a0092-103">Совместное связывание классов</span><span class="sxs-lookup"><span data-stu-id="a0092-103">Linking Classes Together</span></span>

<span data-ttu-id="a0092-104">Поставщики WMI обычно предназначены для предоставления сведений об определенном управляемом объекте на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a0092-104">WMI providers are usually designed to provide information about a specific managed object on a single computer.</span></span> <span data-ttu-id="a0092-105">Если имеется общее свойство, которое может служить ключом для уникальной идентификации всех экземпляров исходного кода, используйте [поставщик представления](view-provider.md) для объединения свойств из разных классов, пространств имен или компьютеров в один класс.</span><span class="sxs-lookup"><span data-stu-id="a0092-105">If there is a common property that can serve as a key to uniquely identify all the different source instances, then use the [View Provider](view-provider.md) to combine properties from different classes, namespaces, or computers into a single class.</span></span>

<span data-ttu-id="a0092-106">Сначала необходимо [зарегистрировать поставщик представления](registering-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a0092-106">You must first [register the View Provider](registering-the-view-provider.md).</span></span> <span data-ttu-id="a0092-107">После регистрации можно создать следующие типы классов представлений:</span><span class="sxs-lookup"><span data-stu-id="a0092-107">After registration, you can create the following types of view classes:</span></span>

-   [<span data-ttu-id="a0092-108">Присоединение к представлению</span><span class="sxs-lookup"><span data-stu-id="a0092-108">Join view</span></span>](creating-a-new-instance-from-old-properties.md)

    <span data-ttu-id="a0092-109">Экземпляры различных классов, Соединенных значением общего свойства.</span><span class="sxs-lookup"><span data-stu-id="a0092-109">Instances of different classes connected by a common property value.</span></span>

-   [<span data-ttu-id="a0092-110">Представление Ассоциации</span><span class="sxs-lookup"><span data-stu-id="a0092-110">Association view</span></span>](associating-instances-between-namespaces.md)

    <span data-ttu-id="a0092-111">Представления существующих классов взаимосвязей по границе пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a0092-111">Views of existing association classes across the namespace boundary.</span></span>

-   [<span data-ttu-id="a0092-112">Представление объединения</span><span class="sxs-lookup"><span data-stu-id="a0092-112">Union view</span></span>](creating-a-union-view-class.md)

    <span data-ttu-id="a0092-113">Объединение одного или нескольких экземпляров.</span><span class="sxs-lookup"><span data-stu-id="a0092-113">Union of one or more instances.</span></span>

 

 



