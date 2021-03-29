---
title: Установка прав доступа ко всему объекту
description: Определенные разрешения могут быть установлены только для всего объекта, например для удаления и вывода списка содержимого. Разрешения, зависящие от операции, такие как разрешение чтение, также можно задать для всего объекта, чтобы они применялись ко всему объекту.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Установка прав доступа для всего объекта Active Directory
- объекты AD, установка прав доступа на
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a965b646de1ee3eba40757386fd243839cb35b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487393"
---
# <a name="setting-access-rights-on-the-entire-object"></a><span data-ttu-id="602b4-106">Установка прав доступа ко всему объекту</span><span class="sxs-lookup"><span data-stu-id="602b4-106">Setting Access Rights on the Entire Object</span></span>

<span data-ttu-id="602b4-107">Определенные разрешения могут быть установлены только для всего объекта, например для удаления и вывода списка содержимого.</span><span class="sxs-lookup"><span data-stu-id="602b4-107">Certain permissions can be set only for an entire object, such as Delete and List Contents.</span></span> <span data-ttu-id="602b4-108">Разрешения, зависящие от операции, такие как разрешение чтение, также можно задать для всего объекта, чтобы они применялись ко всему объекту.</span><span class="sxs-lookup"><span data-stu-id="602b4-108">Operation-specific permissions, such as the Read permission, can also be set for entire object so that they apply to an entire object.</span></span>

<span data-ttu-id="602b4-109">Для установки разрешений для всего объекта можно использовать следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="602b4-109">The following procedure can be used to set permissions for an entire object.</span></span>

<span data-ttu-id="602b4-110">**Установка разрешений для всего объекта**</span><span class="sxs-lookup"><span data-stu-id="602b4-110">**To set permissions for an entire object**</span></span>

1.  <span data-ttu-id="602b4-111">Установите [**иадсакцессконтролентри. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) в **ADS \_ AceType \_ доступ \_ разрешен** или **ADS \_ AceType \_ доступ \_ запрещен**.</span><span class="sxs-lookup"><span data-stu-id="602b4-111">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED** or **ADS\_ACETYPE\_ACCESS\_DENIED**.</span></span>
2.  <span data-ttu-id="602b4-112">Задайте для [**иадсакцессконтролентри. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) и **Иадсакцессконтролентри. инхеритедобжекттипе** **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="602b4-112">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) and **IADsAccessControlEntry.InheritedObjectType** to **NULL**.</span></span>

<span data-ttu-id="602b4-113">Дополнительные сведения о создании элемента управления доступом см. в разделе [Установка прав доступа для объекта](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="602b4-113">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="602b4-114">Дополнительные сведения и пример кода, который можно использовать для установки ACE, см. в разделе [пример кода для настройки элемента управления доступом на объекте каталога](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="602b4-114">For more information and a code example that can be used to set an ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 