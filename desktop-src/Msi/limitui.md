---
description: Если задано свойство ЛИМИТУИ, то уровень пользовательского интерфейса, используемый при установке пакета, ограничен базовым.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: ЛИМИТУИ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685158"
---
# <a name="limitui-property"></a><span data-ttu-id="9fdd7-103">ЛИМИТУИ, свойство</span><span class="sxs-lookup"><span data-stu-id="9fdd7-103">LIMITUI property</span></span>

<span data-ttu-id="9fdd7-104">Если задано свойство **лимитуи** , то уровень пользовательского интерфейса, используемый при установке пакета, ограничен базовым.</span><span class="sxs-lookup"><span data-stu-id="9fdd7-104">If the **LIMITUI** property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span> <span data-ttu-id="9fdd7-105">Это свойство является обязательным в пакетах, которые не имеют созданного пользовательского интерфейса, но по-прежнему содержат таблицы пользовательского интерфейса, такие как [Таблица диалоговых окон](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="9fdd7-105">This property is required in packages that have no authored UI but still contain UI tables such as the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="9fdd7-106">Описание уровней пользовательского интерфейса см. в разделе [ **мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span><span class="sxs-lookup"><span data-stu-id="9fdd7-106">For a description of UI levels, see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span></span>

## <a name="remarks"></a><span data-ttu-id="9fdd7-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fdd7-107">Remarks</span></span>

<span data-ttu-id="9fdd7-108">Пакеты установки, содержащие свойство **лимитуи** , также должны содержать свойство [**арпномодифи**](arpnomodify.md) .</span><span class="sxs-lookup"><span data-stu-id="9fdd7-108">Installation packages containing the **LIMITUI** property must also contain the [**ARPNOMODIFY**](arpnomodify.md) property.</span></span> <span data-ttu-id="9fdd7-109">Это необходимо, чтобы пользователь получил правильное поведение из окна " **Установка и удаление программ** " в служебной программе " **Панель управления** " при попытке настроить продукт.</span><span class="sxs-lookup"><span data-stu-id="9fdd7-109">This is required for a user to obtain the correct behavior from the **Add or Remove Programs** in the **Control Panel** utility when attempting to configure a product.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fdd7-110">Требования</span><span class="sxs-lookup"><span data-stu-id="9fdd7-110">Requirements</span></span>



| <span data-ttu-id="9fdd7-111">Требование</span><span class="sxs-lookup"><span data-stu-id="9fdd7-111">Requirement</span></span> | <span data-ttu-id="9fdd7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9fdd7-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fdd7-113">Версия</span><span class="sxs-lookup"><span data-stu-id="9fdd7-113">Version</span></span><br/> | <span data-ttu-id="9fdd7-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9fdd7-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9fdd7-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9fdd7-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9fdd7-116">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9fdd7-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9fdd7-117">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9fdd7-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fdd7-118">См. также</span><span class="sxs-lookup"><span data-stu-id="9fdd7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fdd7-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="9fdd7-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="9fdd7-120">**мсисетинтерналуи**</span><span class="sxs-lookup"><span data-stu-id="9fdd7-120">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[<span data-ttu-id="9fdd7-121">**арпномодифи**</span><span class="sxs-lookup"><span data-stu-id="9fdd7-121">**ARPNOMODIFY**</span></span>](arpnomodify.md)
</dt> </dl>

 

 




