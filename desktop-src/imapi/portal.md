---
title: API-интерфейс для основного изображения
description: API-интерфейс для основного изображения
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641d9357496eb82a7e30f25a711928b16eeee2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117582"
---
# <a name="image-mastering-api"></a><span data-ttu-id="696d8-103">API-интерфейс для основного изображения</span><span class="sxs-lookup"><span data-stu-id="696d8-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="696d8-104">Цель</span><span class="sxs-lookup"><span data-stu-id="696d8-104">Purpose</span></span>

<span data-ttu-id="696d8-105">API Microsoft Windows для создания образа позволяет приложениям создавать и записывать образы на компакт-дисках, DVD-дисках и оптических носителях.</span><span class="sxs-lookup"><span data-stu-id="696d8-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="696d8-106">Этот API также можно использовать для других дисковых носителей, предназначенных для размещения изображений аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="696d8-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="696d8-107">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="696d8-107">Developer audience</span></span>

<span data-ttu-id="696d8-108">IMAPI предназначен для C/C++ и Visual Basic разработчиков, а также для написания сценариев, использующих VBScript.</span><span class="sxs-lookup"><span data-stu-id="696d8-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="696d8-109">Рекомендуется знание технологий CD, DVD и Blu-Ray и файловых систем.</span><span class="sxs-lookup"><span data-stu-id="696d8-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="696d8-110">Разработчики могут воспользоваться преимуществами последней версии команды мультимедиа (MMC) по адресу [FTP://FTP.T10.org/T10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="696d8-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="696d8-111">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="696d8-111">Run-time requirements</span></span>

<span data-ttu-id="696d8-112">IMAPI 2,0 поддерживается изначально начиная с Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="696d8-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="696d8-113">Для включения функций IMAPI 2,0 для Windows XP и Windows Server 2003 требуется установка пакета обновления [KB932716](https://support.microsoft.com/kb/932716) .</span><span class="sxs-lookup"><span data-stu-id="696d8-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="696d8-114">Если этот пакет не установлен, Windows XP по-прежнему поддерживает [IMAPI 1,0](imapiv1.md).</span><span class="sxs-lookup"><span data-stu-id="696d8-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="696d8-115">Пакет дополнительных компонентов Windows для хранилища доступен для общедоступной версии через [Центр загрузки Майкрософт](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span><span class="sxs-lookup"><span data-stu-id="696d8-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="696d8-116">Дополнительные сведения о конкретных изменениях API можно найти в разделе [новые](what-s-new.md) возможности.</span><span class="sxs-lookup"><span data-stu-id="696d8-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="696d8-117">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="696d8-117">In this section</span></span>



| <span data-ttu-id="696d8-118">Раздел</span><span class="sxs-lookup"><span data-stu-id="696d8-118">Topic</span></span>                                             | <span data-ttu-id="696d8-119">Описание</span><span class="sxs-lookup"><span data-stu-id="696d8-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="696d8-120">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="696d8-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="696d8-121">Сведения о каждом значительном выпуске API для работы с образами.</span><span class="sxs-lookup"><span data-stu-id="696d8-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="696d8-122">О программе IMAPI</span><span class="sxs-lookup"><span data-stu-id="696d8-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="696d8-123">Общие сведения об API-интерфейсе основного образа.</span><span class="sxs-lookup"><span data-stu-id="696d8-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="696d8-124">Использование IMAPI</span><span class="sxs-lookup"><span data-stu-id="696d8-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="696d8-125">Разделы, связанные с задачами, демонстрирующие использование API-интерфейса основного образа.</span><span class="sxs-lookup"><span data-stu-id="696d8-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="696d8-126">Справочник по IMAPI</span><span class="sxs-lookup"><span data-stu-id="696d8-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="696d8-127">Подробное описание интерфейсов IMAPI и других программных элементов.</span><span class="sxs-lookup"><span data-stu-id="696d8-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="696d8-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="696d8-128">Additional resources</span></span>

<span data-ttu-id="696d8-129">Дополнительные сведения о IMAPI и других связанных темах можно найти в следующих расположениях:</span><span class="sxs-lookup"><span data-stu-id="696d8-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="696d8-130">Блог о оптическом хранении (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="696d8-130">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="696d8-131">Основные разделы, в которых основное внимание уделяется реализации API-интерфейса для работы с изображениями в реальных сценариях разработки.</span><span class="sxs-lookup"><span data-stu-id="696d8-131">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="696d8-132">Форум по оптическому платформенному обсуждению</span><span class="sxs-lookup"><span data-stu-id="696d8-132">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="696d8-133">Обсудите CDROM.SYS, IMAPIv2 и динамические вопросы файловой системы.</span><span class="sxs-lookup"><span data-stu-id="696d8-133">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="696d8-134">Этот форум посвящен темам на уровне системы и предназначен для разработчиков приложений, а не вынужденным.</span><span class="sxs-lookup"><span data-stu-id="696d8-134">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="696d8-135">Технический Комитет T10</span><span class="sxs-lookup"><span data-stu-id="696d8-135">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="696d8-136">Технический комитет Международного комитета по стандартам информационных технологий (ИНЦИТС, произносится «Insights»).</span><span class="sxs-lookup"><span data-stu-id="696d8-136">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="696d8-137">ИНЦИТС аккредитованное by и работает с правилами, утвержденными, Американский национальный институт стандартов (ANSI) (ANSI).</span><span class="sxs-lookup"><span data-stu-id="696d8-137">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="696d8-138">Эти правила предназначены для того, чтобы обеспечить разработку добровольных стандартов в отношении отраслевых групп.</span><span class="sxs-lookup"><span data-stu-id="696d8-138">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="696d8-139">Ассоциация технологии оптического хранилища (ОСТА)</span><span class="sxs-lookup"><span data-stu-id="696d8-139">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="696d8-140">Работает, чтобы сформировать будущее отрасли с помощью обычных совещаний коммерческих приложений для оптического хранения (коса), совместимости DVD, маркетинга, MPV (Мусикфотовидео), специализированных комитетов и нового прямого лазерного Комитета.</span><span class="sxs-lookup"><span data-stu-id="696d8-140">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="696d8-141">Заинтересованные компании по всему миру приглашаются к Организации и участвуют в своих комитетах и программах.</span><span class="sxs-lookup"><span data-stu-id="696d8-141">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 

