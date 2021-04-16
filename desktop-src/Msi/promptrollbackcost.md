---
description: 'Свойство ПРОМПТРОЛЛБАКККОСТ указывает действие, которое требуется установщику, если включены возможности установки отката и недостаточно места на диске для завершения установки. Возможные значения ПРОМПТРОЛЛБАКККОСТ: Валуеактионпдисплай диалоговое окно с вопросом, следует ли продолжить без отката. Ддисабле откат и продолжайте без запроса пользователя. Ффаил с запросом об ошибке нехватки места на диске.'
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: ПРОМПТРОЛЛБАКККОСТ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652186"
---
# <a name="promptrollbackcost-property"></a><span data-ttu-id="9e699-103">ПРОМПТРОЛЛБАКККОСТ, свойство</span><span class="sxs-lookup"><span data-stu-id="9e699-103">PROMPTROLLBACKCOST property</span></span>

<span data-ttu-id="9e699-104">Свойство **промптроллбакккост** указывает действие, которое требуется установщику, если включены возможности [установки отката](rollback-installation.md) и недостаточно места на диске для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="9e699-104">The **PROMPTROLLBACKCOST** property specifies the action the installer takes if [rollback installation](rollback-installation.md) capabilities are enabled and there is insufficient disk space to complete the installation.</span></span>

<span data-ttu-id="9e699-105">Возможные значения **промптроллбакккост** :</span><span class="sxs-lookup"><span data-stu-id="9e699-105">The possible values of **PROMPTROLLBACKCOST** are as follows.</span></span>



| <span data-ttu-id="9e699-106">Значение</span><span class="sxs-lookup"><span data-stu-id="9e699-106">Value</span></span> | <span data-ttu-id="9e699-107">Действие</span><span class="sxs-lookup"><span data-stu-id="9e699-107">Action</span></span>                                                              |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="9e699-108">С</span><span class="sxs-lookup"><span data-stu-id="9e699-108">P</span></span>     | <span data-ttu-id="9e699-109">Отображение диалогового окна с вопросом, следует ли продолжить без отката.</span><span class="sxs-lookup"><span data-stu-id="9e699-109">Display a dialog box asking whether to continue without a rollback.</span></span> |
| <span data-ttu-id="9e699-110">D</span><span class="sxs-lookup"><span data-stu-id="9e699-110">D</span></span>     | <span data-ttu-id="9e699-111">Отключите откат и продолжайте, не запрашивая пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e699-111">Disable rollback and continue without asking user.</span></span>                  |
| <span data-ttu-id="9e699-112">C</span><span class="sxs-lookup"><span data-stu-id="9e699-112">F</span></span>     | <span data-ttu-id="9e699-113">Завершается с запросом об ошибке нехватки места на диске.</span><span class="sxs-lookup"><span data-stu-id="9e699-113">Fail with the out-of-disk-space error prompt.</span></span>                       |



 

## <a name="remarks"></a><span data-ttu-id="9e699-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e699-114">Remarks</span></span>

<span data-ttu-id="9e699-115">Когда пользовательский интерфейс запускается на уровне Basic или без пользовательского интерфейса, установщик обрабатывает всю логику вне места на диске автоматически.</span><span class="sxs-lookup"><span data-stu-id="9e699-115">When the user interface is run at the Basic or no UI level, the installer handles all the out-of-disk-space logic automatically.</span></span>

<span data-ttu-id="9e699-116">Когда пользовательский интерфейс выполняется на полном уровне, пользователю могут быть предоставлены дополнительные параметры, такие как запрос перед выполнением отката, отключение отката или продолжение без отката при заполнении диска.</span><span class="sxs-lookup"><span data-stu-id="9e699-116">When the user interface runs at the Full level, the user can be given additional options, such as prompting before proceeding with a rollback, disabling rollback, or proceeding without rollback when the disk is full.</span></span> <span data-ttu-id="9e699-117">Разработчику пакета необходимо разработать последовательность диалоговых окон, чтобы предоставить пользователю соответствующие варианты.</span><span class="sxs-lookup"><span data-stu-id="9e699-117">It is up to the package developer to author the dialog box sequence to provide the appropriate choices to the user.</span></span> <span data-ttu-id="9e699-118">Доступные для этого элементы: [Енаблероллбакк таблице ControlEvent событие](enablerollback-controlevent.md), свойство [**Аутофдискспаце**](outofdiskspace.md) , свойство [**аутофнорбдискспаце**](outofnorbdiskspace.md) и свойство **промптроллбакккост** .</span><span class="sxs-lookup"><span data-stu-id="9e699-118">The elements available to do this are the [EnableRollback ControlEvent](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) property, [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property, and the **PROMPTROLLBACKCOST** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e699-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9e699-119">Requirements</span></span>



| <span data-ttu-id="9e699-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9e699-120">Requirement</span></span> | <span data-ttu-id="9e699-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9e699-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e699-122">Версия</span><span class="sxs-lookup"><span data-stu-id="9e699-122">Version</span></span><br/> | <span data-ttu-id="9e699-123">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9e699-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9e699-124">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e699-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9e699-125">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9e699-125">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9e699-126">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9e699-126">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e699-127">См. также</span><span class="sxs-lookup"><span data-stu-id="9e699-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e699-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="9e699-128">Properties</span></span>](properties.md)
</dt> </dl>

 

 




