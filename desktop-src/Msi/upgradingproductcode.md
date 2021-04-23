---
description: Свойство УПГРАДИНГПРОДУКТКОДЕ задается установщик Windows, когда обновление удаляет приложение.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: УПГРАДИНГПРОДУКТКОДЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651901"
---
# <a name="upgradingproductcode-property"></a><span data-ttu-id="c3b89-103">УПГРАДИНГПРОДУКТКОДЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="c3b89-103">UPGRADINGPRODUCTCODE property</span></span>

<span data-ttu-id="c3b89-104">Свойство **упградингпродукткоде** задается установщик Windows, когда обновление удаляет приложение.</span><span class="sxs-lookup"><span data-stu-id="c3b89-104">The **UPGRADINGPRODUCTCODE** property is set by Windows Installer when an upgrade removes an application.</span></span> <span data-ttu-id="c3b89-105">Установщик задает это свойство при выполнении [действия RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="c3b89-105">The installer sets this property when it runs the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="c3b89-106">Это свойство не задается путем удаления приложения с помощью компонента "Установка и удаление программ" панели управления.</span><span class="sxs-lookup"><span data-stu-id="c3b89-106">This property is not set by removing an application using the Add or Remove Programs in Control Panel.</span></span> <span data-ttu-id="c3b89-107">Приложение определяет, будет ли оно удалено обновлением или компонентом Установка и удаление программ путем проверки **упградингпродукткоде**.</span><span class="sxs-lookup"><span data-stu-id="c3b89-107">An application determines whether it is being removed by an upgrade or the Add or Remove Programs by checking **UPGRADINGPRODUCTCODE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3b89-108">Требования</span><span class="sxs-lookup"><span data-stu-id="c3b89-108">Requirements</span></span>



| <span data-ttu-id="c3b89-109">Требование</span><span class="sxs-lookup"><span data-stu-id="c3b89-109">Requirement</span></span> | <span data-ttu-id="c3b89-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c3b89-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b89-111">Версия</span><span class="sxs-lookup"><span data-stu-id="c3b89-111">Version</span></span><br/> | <span data-ttu-id="c3b89-112">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3b89-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c3b89-113">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3b89-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c3b89-114">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3b89-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c3b89-115">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c3b89-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3b89-116">См. также</span><span class="sxs-lookup"><span data-stu-id="c3b89-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3b89-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="c3b89-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




