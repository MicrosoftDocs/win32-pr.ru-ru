---
description: Это установщик Windows свойство указывает, когда уровень внутреннего пользовательского интерфейса был установлен на скрытие кнопки отмены.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Мсиуихидеканцел, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679610"
---
# <a name="msiuihidecancel-property"></a><span data-ttu-id="94672-103">Мсиуихидеканцел, свойство</span><span class="sxs-lookup"><span data-stu-id="94672-103">MsiUIHideCancel property</span></span>

<span data-ttu-id="94672-104">Установщик задает для свойства **мсиуихидеканцел** значение 1, если на уровне внутреннего пользовательского интерфейса задано включение инсталлуилевел \_ Хидеканцел с функцией [**Мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) или свойством [Duilevel](installer-uilevel.md)объекта [**установщика**](installer-object.md) или с помощью [параметров командной строки](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="94672-104">The installer sets the **MsiUIHideCancel** property to 1 when the internal user interface level has been set to include INSTALLUILEVEL\_HIDECANCEL with the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function or the [UILevel](installer-uilevel.md)property of the [**Installer**](installer-object.md) object or by using [Command Line Options](command-line-options.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94672-105">Требования</span><span class="sxs-lookup"><span data-stu-id="94672-105">Requirements</span></span>



| <span data-ttu-id="94672-106">Требование</span><span class="sxs-lookup"><span data-stu-id="94672-106">Requirement</span></span> | <span data-ttu-id="94672-107">Значение</span><span class="sxs-lookup"><span data-stu-id="94672-107">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94672-108">Версия</span><span class="sxs-lookup"><span data-stu-id="94672-108">Version</span></span><br/> | <span data-ttu-id="94672-109">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="94672-109">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="94672-110">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="94672-110">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="94672-111">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="94672-111">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="94672-112">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="94672-112">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94672-113">См. также</span><span class="sxs-lookup"><span data-stu-id="94672-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94672-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="94672-114">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="94672-115">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="94672-115">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




