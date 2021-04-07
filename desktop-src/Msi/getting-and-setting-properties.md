---
description: Чтобы использовать свойства в установке служб, можно получать и устанавливать значения свойств из программ, использующих MsiGetProperty и MsiSetProperty, и включать их как часть условных операторов в базу данных установки.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Получение и задание свойств (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0154b84af656d295b9fa84ebcca881eab1c288f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910947"
---
# <a name="getting-and-setting-properties-windows-installer"></a><span data-ttu-id="485f5-103">Получение и задание свойств (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="485f5-103">Getting and Setting Properties (Windows Installer)</span></span>

<span data-ttu-id="485f5-104">Чтобы использовать [Свойства](properties.md) в установке служб, можно получать и устанавливать значения свойств из программ, использующих [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) и [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) , и включать их как часть условных операторов в базу данных установки.</span><span class="sxs-lookup"><span data-stu-id="485f5-104">To use [properties](properties.md) in your installation, you can get and set property values from programs using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) and [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) and include as part of conditional statements in the installation database.</span></span>

-   <span data-ttu-id="485f5-105">Чтобы получить текущее свойство, вызовите функцию [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) .</span><span class="sxs-lookup"><span data-stu-id="485f5-105">To obtain a current property, call the [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) function.</span></span>
-   <span data-ttu-id="485f5-106">Чтобы получить текущее состояние установки, вызовите функцию [**мсижетмоде**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .</span><span class="sxs-lookup"><span data-stu-id="485f5-106">To obtain the current installation state, call the [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function.</span></span>
-   <span data-ttu-id="485f5-107">Чтобы получить язык для текущей установки, вызовите функцию [**мсижетлангуаже**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) .</span><span class="sxs-lookup"><span data-stu-id="485f5-107">To obtain the language for the current installation, call the [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) function.</span></span>
-   <span data-ttu-id="485f5-108">Чтобы задать свойство, вызовите функцию [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) .</span><span class="sxs-lookup"><span data-stu-id="485f5-108">To set a property, call the [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) function.</span></span>
-   <span data-ttu-id="485f5-109">Чтобы задать состояние установки, вызовите функцию [**мсисетмоде**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) .</span><span class="sxs-lookup"><span data-stu-id="485f5-109">To set the installation state, call the [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) function.</span></span>
-   <span data-ttu-id="485f5-110">Чтобы очистить свойство (присвоив ему значение null), задайте в качестве значения свойства пустую строку: "".</span><span class="sxs-lookup"><span data-stu-id="485f5-110">To clear a property (setting it to Null), set the property's value to an empty string: "".</span></span>

## <a name="related-topics"></a><span data-ttu-id="485f5-111">См. также</span><span class="sxs-lookup"><span data-stu-id="485f5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="485f5-112">Использование свойств</span><span class="sxs-lookup"><span data-stu-id="485f5-112">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="485f5-113">Установка значений открытых свойств в командной строке</span><span class="sxs-lookup"><span data-stu-id="485f5-113">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="485f5-114">Очистка свойства установщика</span><span class="sxs-lookup"><span data-stu-id="485f5-114">Clearing an Installer Property</span></span>](clearing-an-installer-property.md)
</dt> </dl>

 

 



