---
description: Если для этой системной политики на уровне компьютера задано значение 1, ни один из пакетов в системе не получает функции общего компонента, включенные атрибутом Мсидбкомпонентаттрибутесшаред в таблице Component.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: дисаблешаредкомпонент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542743"
---
# <a name="disablesharedcomponent"></a><span data-ttu-id="a6b00-103">дисаблешаредкомпонент</span><span class="sxs-lookup"><span data-stu-id="a6b00-103">DisableSharedComponent</span></span>

<span data-ttu-id="a6b00-104">Если для этой [системной политики](system-policy.md) на уровне компьютера задано значение 1, ни один из пакетов в системе не получает функции общего компонента, включенные атрибутом **Мсидбкомпонентаттрибутесшаред** в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a6b00-104">If this per-machine [system policy](system-policy.md) is set to 1, no package on the system gets the shared component functionality enabled by the **msidbComponentAttributesShared** attribute in the [Component table](component-table.md).</span></span> <span data-ttu-id="a6b00-105">Значение по умолчанию — 0, что обеспечивает функциональность общего компонента для компонентов, помеченных **мсидбкомпонентаттрибутесшаред** во всех пакетах.</span><span class="sxs-lookup"><span data-stu-id="a6b00-105">The default value is 0, which enables the shared component functionality for components marked with **msidbComponentAttributesShared** in all packages.</span></span>

<span data-ttu-id="a6b00-106">**[Установщик Windows 4,0 и более ранних версий](not-supported-in-windows-installer-4-0.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a6b00-106">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="a6b00-107">Эта функция доступна начиная с установщик Windows 4,5.</span><span class="sxs-lookup"><span data-stu-id="a6b00-107">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="a6b00-108">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="a6b00-108">Registry Key</span></span>

<span data-ttu-id="a6b00-109">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="a6b00-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="a6b00-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a6b00-110">Data Type</span></span>

<span data-ttu-id="a6b00-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a6b00-111">**REG\_DWORD**</span></span>

 

 



