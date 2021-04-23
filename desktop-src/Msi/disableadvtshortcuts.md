---
description: Установка свойства ДИСАБЛЕАДВТШОРТКУТС отключает создание ярлыков, поддерживающих установку по запросу и объявление. Задание этого свойства указывает, что эти сочетания клавиш следует заменить обычными сочетаниями клавиш.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: ДИСАБЛЕАДВТШОРТКУТС, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651581"
---
# <a name="disableadvtshortcuts-property"></a><span data-ttu-id="81f36-104">ДИСАБЛЕАДВТШОРТКУТС, свойство</span><span class="sxs-lookup"><span data-stu-id="81f36-104">DISABLEADVTSHORTCUTS property</span></span>

<span data-ttu-id="81f36-105">Установка свойства **дисаблеадвтшорткутс** отключает создание ярлыков, поддерживающих [установку по запросу](installation-on-demand.md) и [объявление](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="81f36-105">Setting the **DISABLEADVTSHORTCUTS** property disables the generation of shortcuts supporting [installation-on-demand](installation-on-demand.md) and [advertisement](advertisement.md).</span></span> <span data-ttu-id="81f36-106">Задание этого свойства указывает, что эти сочетания клавиш следует заменить обычными сочетаниями клавиш.</span><span class="sxs-lookup"><span data-stu-id="81f36-106">Setting this property specifies that these shortcuts should instead be replaced by regular shortcuts.</span></span>

## <a name="default-value"></a><span data-ttu-id="81f36-107">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="81f36-107">Default Value</span></span>

<span data-ttu-id="81f36-108">По умолчанию создание ярлыка по запросу включено.</span><span class="sxs-lookup"><span data-stu-id="81f36-108">By default, installation-on-demand shortcut generation is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="81f36-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81f36-109">Remarks</span></span>

<span data-ttu-id="81f36-110">Сочетания клавиш, которые поддерживают объявление, имеют имя функции, а не форматированный путь к файлу формы \[ \# филекэй \] , введенный в столбец Target [таблицы ярлыков](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="81f36-110">The shortcuts that support advertisement have the name of a feature, rather than a formatted file path of the form \[\#filekey\], entered in the Target column of the [Shortcut table](shortcut-table.md).</span></span> <span data-ttu-id="81f36-111">Если это свойство задано и компонент установлен, установщик создает регулярное сочетание для компонента.</span><span class="sxs-lookup"><span data-stu-id="81f36-111">If this property is set and the feature is installed, the installer generates a regular shortcut to the feature.</span></span>

<span data-ttu-id="81f36-112">Это свойство обычно используется администраторами для пользователей, которые перемещаются между средами, которые выполняют и не поддерживают рекламу.</span><span class="sxs-lookup"><span data-stu-id="81f36-112">This property is commonly used by administrators for users who roam between environments that do and do not support advertising.</span></span> <span data-ttu-id="81f36-113">Это свойство может быть задано преобразованием, в административном потоке или в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="81f36-113">This property can be set by a transform, in the administrative stream, or in the [Property table](property-table.md).</span></span> <span data-ttu-id="81f36-114">Если он задан с помощью командной строки или вызова [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), он должен быть сброшен повторно во время каждой последующей установки.</span><span class="sxs-lookup"><span data-stu-id="81f36-114">If it is set using the command line or by a call to [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), then it must be reset again during each subsequent installation.</span></span>

## <a name="requirements"></a><span data-ttu-id="81f36-115">Требования</span><span class="sxs-lookup"><span data-stu-id="81f36-115">Requirements</span></span>



| <span data-ttu-id="81f36-116">Требование</span><span class="sxs-lookup"><span data-stu-id="81f36-116">Requirement</span></span> | <span data-ttu-id="81f36-117">Значение</span><span class="sxs-lookup"><span data-stu-id="81f36-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81f36-118">Версия</span><span class="sxs-lookup"><span data-stu-id="81f36-118">Version</span></span><br/> | <span data-ttu-id="81f36-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="81f36-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="81f36-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="81f36-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="81f36-121">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="81f36-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="81f36-122">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="81f36-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81f36-123">См. также</span><span class="sxs-lookup"><span data-stu-id="81f36-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81f36-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="81f36-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




