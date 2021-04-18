---
title: Сведения о версиях моделей объектов
description: Сведения о версиях моделей объектов
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Проигрыватель Windows Media, версии
- Объектная модель проигрывателя Windows Media, версии
- Объектная модель, версии
- Элемент управления ActiveX проигрывателя Windows Media, версии для объектной модели
- Элемент управления ActiveX, версии для объектной модели
- Элемент управления ActiveX мобильных устройств проигрывателя Windows Media, версии для объектной модели
- Проигрыватель Windows Media Mobile, версии для объектной модели
- версии проигрывателя Windows Media, объектная модель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59886f5750b6fc42112f73d6bb6e05e8d013ffdc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "104412688"
---
# <a name="about-the-object-model-versions"></a><span data-ttu-id="dacca-111">Сведения о версиях моделей объектов</span><span class="sxs-lookup"><span data-stu-id="dacca-111">About the Object Model Versions</span></span>

<span data-ttu-id="dacca-112">В проигрывателе Windows Media 7,0 появилась новая объектная модель.</span><span class="sxs-lookup"><span data-stu-id="dacca-112">Windows Media Player 7.0 introduced a new object model.</span></span> <span data-ttu-id="dacca-113">Эта объектная модель была расширена с помощью проигрывателя Windows Media 7,1, проигрывателя Windows Media для Windows XP, проигрывателя Windows Media 9 Series, проигрывателя Windows Media 10, проигрывателя Windows Media 11 и проигрывателя Windows Media 12.</span><span class="sxs-lookup"><span data-stu-id="dacca-113">This object model has been extended with Windows Media Player 7.1, Windows Media Player for Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11, and Windows Media Player 12.</span></span> <span data-ttu-id="dacca-114">Каждый раздел в справочнике по объектной модели содержит раздел требований, в котором подробно описаны минимальные требования к отдельному свойству, методу или событию.</span><span class="sxs-lookup"><span data-stu-id="dacca-114">Each topic in the Object Model Reference includes a Requirements section that details the minimum requirement for the individual property, method, or event.</span></span> <span data-ttu-id="dacca-115">Ниже приведены сведения о новых объектах, методах, свойствах и событиях, которые были добавлены для каждой версии с момента выпуска версии 7,0.</span><span class="sxs-lookup"><span data-stu-id="dacca-115">The following lists detail the new objects, methods, properties, and events that have been added for each version since version 7.0.</span></span> <span data-ttu-id="dacca-116">В эти списки также входят новые интерфейсы, методы и события C++.</span><span class="sxs-lookup"><span data-stu-id="dacca-116">These lists also include new C++ interfaces, methods, and events.</span></span>

<span data-ttu-id="dacca-117">Когда новый или обновленный интерфейс также предоставляется как объект, в списке отображается только объект.</span><span class="sxs-lookup"><span data-stu-id="dacca-117">Where a new or updated interface is also exposed as an object, only the object is listed.</span></span> <span data-ttu-id="dacca-118">Чтобы найти интерфейс, обратитесь к [Справочнику по объектной модели для C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="dacca-118">To locate the interface, refer to the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span> <span data-ttu-id="dacca-119">Как правило, необходимо просто добавить префикс ИВМП в имя объекта.</span><span class="sxs-lookup"><span data-stu-id="dacca-119">Usually, you will simply need to add the IWMP prefix to the object name.</span></span> <span data-ttu-id="dacca-120">Если новый интерфейс расширяет существующий, может потребоваться найти номер последней версии.</span><span class="sxs-lookup"><span data-stu-id="dacca-120">If a new interface extends an existing one, you may need to look for the latest version number.</span></span> <span data-ttu-id="dacca-121">Например, в серии проигрывателя Windows Media 9 появились новые свойства и методы, доступные в объекте [**Settings**](settings-object.md) .</span><span class="sxs-lookup"><span data-stu-id="dacca-121">For example, Windows Media Player 9 Series introduced new properties and methods available from the [**Settings**](settings-object.md) object.</span></span> <span data-ttu-id="dacca-122">В C++ они доступны через интерфейс [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) , который расширяет [**ивмпсеттингс**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span><span class="sxs-lookup"><span data-stu-id="dacca-122">In C++, these are available through the [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) interface, which extends [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span></span>

## <a name="added-for-windows-media-player-71"></a><span data-ttu-id="dacca-123">Добавлено для проигрывателя Windows Media 7,1</span><span class="sxs-lookup"><span data-stu-id="dacca-123">Added for Windows Media Player 7.1</span></span>

-   [<span data-ttu-id="dacca-124">**Свойство Player. Стретчтофит**</span><span class="sxs-lookup"><span data-stu-id="dacca-124">**Player.stretchToFit Property**</span></span>](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a><span data-ttu-id="dacca-125">Добавлено для проигрывателя Windows Media для Windows XP</span><span class="sxs-lookup"><span data-stu-id="dacca-125">Added for Windows Media Player for Windows XP</span></span>

-   [<span data-ttu-id="dacca-126">**Метод Controls. Step**</span><span class="sxs-lookup"><span data-stu-id="dacca-126">**Controls.step Method**</span></span>](controls-step.md)
-   [<span data-ttu-id="dacca-127">**Объект DVD**</span><span class="sxs-lookup"><span data-stu-id="dacca-127">**DVD Object**</span></span>](dvd-object.md)
-   [<span data-ttu-id="dacca-128">**Свойство Media. Error**</span><span class="sxs-lookup"><span data-stu-id="dacca-128">**Media.error Property**</span></span>](media-error.md)
-   [<span data-ttu-id="dacca-129">**Событие Player. Домаинчанже**</span><span class="sxs-lookup"><span data-stu-id="dacca-129">**Player.DomainChange Event**</span></span>](player-player-domainchange.md)
-   [<span data-ttu-id="dacca-130">**Событие Player. Медиаеррор**</span><span class="sxs-lookup"><span data-stu-id="dacca-130">**Player.MediaError Event**</span></span>](player-player-mediaerror.md)
-   [<span data-ttu-id="dacca-131">**Событие Player. Опенплайлистсвитч**</span><span class="sxs-lookup"><span data-stu-id="dacca-131">**Player.OpenPlaylistSwitch Event**</span></span>](player-player-openplaylistswitch.md)
-   [<span data-ttu-id="dacca-132">**Свойство Player. Виндовлессвидео**</span><span class="sxs-lookup"><span data-stu-id="dacca-132">**Player.windowlessVideo Property**</span></span>](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a><span data-ttu-id="dacca-133">Добавлено для проигрывателя Windows Media 9 Series</span><span class="sxs-lookup"><span data-stu-id="dacca-133">Added for Windows Media Player 9 Series</span></span>

-   [<span data-ttu-id="dacca-134">**Клоседкаптион. Жетсамилангид, метод**</span><span class="sxs-lookup"><span data-stu-id="dacca-134">**ClosedCaption.getSAMILangID Method**</span></span>](closedcaption-getsamilangid.md)
-   [<span data-ttu-id="dacca-135">**Клоседкаптион. Жетсамилангнаме, метод**</span><span class="sxs-lookup"><span data-stu-id="dacca-135">**ClosedCaption.getSAMILangName Method**</span></span>](closedcaption-getsamilangname.md)
-   [<span data-ttu-id="dacca-136">**Клоседкаптион. Жетсамистиленаме, метод**</span><span class="sxs-lookup"><span data-stu-id="dacca-136">**ClosedCaption.getSAMIStyleName Method**</span></span>](closedcaption-getsamistylename.md)
-   [<span data-ttu-id="dacca-137">**Клоседкаптион. Самилангкаунт, свойство**</span><span class="sxs-lookup"><span data-stu-id="dacca-137">**ClosedCaption.SAMILangCount Property**</span></span>](closedcaption-samilangcount.md)
-   [<span data-ttu-id="dacca-138">**Клоседкаптион. Самистилекаунт, свойство**</span><span class="sxs-lookup"><span data-stu-id="dacca-138">**ClosedCaption.SAMIStyleCount Property**</span></span>](closedcaption-samistylecount.md)
-   [<span data-ttu-id="dacca-139">**Свойство Controls. Аудиолангуажекаунт**</span><span class="sxs-lookup"><span data-stu-id="dacca-139">**Controls.audioLanguageCount Property**</span></span>](controls-audiolanguagecount.md)
-   [<span data-ttu-id="dacca-140">**Свойство Controls. Куррентаудиолангуаже**</span><span class="sxs-lookup"><span data-stu-id="dacca-140">**Controls.currentAudioLanguage Property**</span></span>](controls-currentaudiolanguage.md)
-   [<span data-ttu-id="dacca-141">**Свойство Controls. Куррентаудиолангуажеиндекс**</span><span class="sxs-lookup"><span data-stu-id="dacca-141">**Controls.currentAudioLanguageIndex Property**</span></span>](controls-currentaudiolanguageindex.md)
-   [<span data-ttu-id="dacca-142">**Свойство Controls. Куррентпоситионтимекоде**</span><span class="sxs-lookup"><span data-stu-id="dacca-142">**Controls.currentPositionTimecode Property**</span></span>](controls-currentpositiontimecode.md)
-   [<span data-ttu-id="dacca-143">**Controls. Жетаудиолангуажедескриптион, метод**</span><span class="sxs-lookup"><span data-stu-id="dacca-143">**Controls.getAudioLanguageDescription Method**</span></span>](controls-getaudiolanguagedescription.md)
-   [<span data-ttu-id="dacca-144">**Controls. Жетаудиолангуажеид, метод**</span><span class="sxs-lookup"><span data-stu-id="dacca-144">**Controls.getAudioLanguageID Method**</span></span>](controls-getaudiolanguageid.md)
-   [<span data-ttu-id="dacca-145">**Controls. Жетлангуаженаме, метод**</span><span class="sxs-lookup"><span data-stu-id="dacca-145">**Controls.getLanguageName Method**</span></span>](controls-getlanguagename.md)
-   [<span data-ttu-id="dacca-146">**Ерроритем. Condition, свойство**</span><span class="sxs-lookup"><span data-stu-id="dacca-146">**ErrorItem.condition Property**</span></span>](erroritem-condition.md)
-   [<span data-ttu-id="dacca-147">**Свойство external. Аппколорлигхт**</span><span class="sxs-lookup"><span data-stu-id="dacca-147">**External.appColorLight Property**</span></span>](external-appcolorlight.md)
-   [<span data-ttu-id="dacca-148">**Внешнее событие Онколорчанже**</span><span class="sxs-lookup"><span data-stu-id="dacca-148">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
-   [<span data-ttu-id="dacca-149">**Свойство external. Version**</span><span class="sxs-lookup"><span data-stu-id="dacca-149">**External.version Property**</span></span>](external-version.md)
-   [<span data-ttu-id="dacca-150">**Ивмпевентс: событие Лайердоккедстатечанже:P**</span><span class="sxs-lookup"><span data-stu-id="dacca-150">**IWMPEvents::PlayerDockedStateChange Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [<span data-ttu-id="dacca-151">**Ивмпевентс: событие Лайерреконнект:P**</span><span class="sxs-lookup"><span data-stu-id="dacca-151">**IWMPEvents::PlayerReconnect Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [<span data-ttu-id="dacca-152">**Событие Ивмпевентс:: Свитчедтоконтрол**</span><span class="sxs-lookup"><span data-stu-id="dacca-152">**IWMPEvents::SwitchedToControl Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [<span data-ttu-id="dacca-153">**Событие Ивмпевентс:: Свитчедтоплайераппликатион**</span><span class="sxs-lookup"><span data-stu-id="dacca-153">**IWMPEvents::SwitchedToPlayerApplication Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [<span data-ttu-id="dacca-154">**Интерфейс Ивмпплайерсервицес**</span><span class="sxs-lookup"><span data-stu-id="dacca-154">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [<span data-ttu-id="dacca-155">**Интерфейс Ивмпремотемедиасервицес**</span><span class="sxs-lookup"><span data-stu-id="dacca-155">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [<span data-ttu-id="dacca-156">**Интерфейс Ивмпскинманажер**</span><span class="sxs-lookup"><span data-stu-id="dacca-156">**IWMPSkinManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [<span data-ttu-id="dacca-157">**Метод Media. Жетаттрибутекаунтбитипе**</span><span class="sxs-lookup"><span data-stu-id="dacca-157">**Media.getAttributeCountByType Method**</span></span>](media-getattributecountbytype.md)
-   [<span data-ttu-id="dacca-158">**Метод Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="dacca-158">**Media.getItemInfoByType Method**</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="dacca-159">**Объект Метадатапиктуре**</span><span class="sxs-lookup"><span data-stu-id="dacca-159">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
-   [<span data-ttu-id="dacca-160">**Объект Метадататекст**</span><span class="sxs-lookup"><span data-stu-id="dacca-160">**MetadataText Object**</span></span>](metadatatext-object.md)
-   [<span data-ttu-id="dacca-161">**Событие Player. Аудиолангуажечанже**</span><span class="sxs-lookup"><span data-stu-id="dacca-161">**Player.AudioLanguageChange Event**</span></span>](player-player-audiolanguagechange.md)
-   [<span data-ttu-id="dacca-162">**Свойство Player. Remote**</span><span class="sxs-lookup"><span data-stu-id="dacca-162">**Player.isRemote Property**</span></span>](player-isremote.md)
-   [<span data-ttu-id="dacca-163">**Событие Player. Медиаколлектионаттрибутестрингчанжед**</span><span class="sxs-lookup"><span data-stu-id="dacca-163">**Player.MediaCollectionAttributeStringChanged Event**</span></span>](player-player-mediacollectionattributestringchanged.md)
-   [<span data-ttu-id="dacca-164">**Метод Player. Невмедиа**</span><span class="sxs-lookup"><span data-stu-id="dacca-164">**Player.newMedia Method**</span></span>](player-newmedia.md)
-   [<span data-ttu-id="dacca-165">**Метод Player. Невплайлист**</span><span class="sxs-lookup"><span data-stu-id="dacca-165">**Player.newPlaylist Method**</span></span>](player-newplaylist.md)
-   [<span data-ttu-id="dacca-166">**Метод Player. Опенплайер**</span><span class="sxs-lookup"><span data-stu-id="dacca-166">**Player.openPlayer Method**</span></span>](player-openplayer.md)
-   [<span data-ttu-id="dacca-167">**Свойство Player. Плайераппликатион**</span><span class="sxs-lookup"><span data-stu-id="dacca-167">**Player.playerApplication Property**</span></span>](player-playerapplication.md)
-   [<span data-ttu-id="dacca-168">**Событие Player. StatusChange**</span><span class="sxs-lookup"><span data-stu-id="dacca-168">**Player.StatusChange Event**</span></span>](player-player-statuschange.md)
-   [<span data-ttu-id="dacca-169">**Объект Плайераппликатион**</span><span class="sxs-lookup"><span data-stu-id="dacca-169">**PlayerApplication Object**</span></span>](playerapplication-object.md)
-   [<span data-ttu-id="dacca-170">**Свойство Settings. Дефаултаудиолангуаже**</span><span class="sxs-lookup"><span data-stu-id="dacca-170">**Settings.defaultAudioLanguage Property**</span></span>](settings-defaultaudiolanguage.md)
-   [<span data-ttu-id="dacca-171">**Свойство Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="dacca-171">**Settings.mediaAccessRights Property**</span></span>](settings-mediaaccessrights.md)
-   [<span data-ttu-id="dacca-172">**Метод Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="dacca-172">**Settings.requestMediaAccessRights Method**</span></span>](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a><span data-ttu-id="dacca-173">Добавлено для проигрывателя Windows Media 10</span><span class="sxs-lookup"><span data-stu-id="dacca-173">Added for Windows Media Player 10</span></span>

-   [<span data-ttu-id="dacca-174">**Интерфейс Ивмпграфкреатион**</span><span class="sxs-lookup"><span data-stu-id="dacca-174">**IWMPGraphCreation Interface**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [<span data-ttu-id="dacca-175">**Интерфейс IWMPPlayerServices2**</span><span class="sxs-lookup"><span data-stu-id="dacca-175">**IWMPPlayerServices2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [<span data-ttu-id="dacca-176">**Интерфейс Ивмпсинкдевице**</span><span class="sxs-lookup"><span data-stu-id="dacca-176">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [<span data-ttu-id="dacca-177">**Интерфейс Ивмпсинксервицес**</span><span class="sxs-lookup"><span data-stu-id="dacca-177">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [<span data-ttu-id="dacca-178">**Перечисление Вмпдевицестатус**</span><span class="sxs-lookup"><span data-stu-id="dacca-178">**WMPDeviceStatus Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [<span data-ttu-id="dacca-179">**Перечисление Вмпсинкстате**</span><span class="sxs-lookup"><span data-stu-id="dacca-179">**WMPSyncState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a><span data-ttu-id="dacca-180">Добавлено для проигрывателя Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="dacca-180">Added for Windows Media Player 11</span></span>

-   [<span data-ttu-id="dacca-181">**Интерфейс Ивмпкдромбурн**</span><span class="sxs-lookup"><span data-stu-id="dacca-181">**IWMPCdromBurn Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [<span data-ttu-id="dacca-182">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dacca-182">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
-   [<span data-ttu-id="dacca-183">**Интерфейс Ивмпкдромрип**</span><span class="sxs-lookup"><span data-stu-id="dacca-183">**IWMPCdromRip Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [<span data-ttu-id="dacca-184">**Интерфейс Ивмпкдромрип (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dacca-184">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
-   [<span data-ttu-id="dacca-185">**Интерфейс IWMPEvents3**</span><span class="sxs-lookup"><span data-stu-id="dacca-185">**IWMPEvents3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [<span data-ttu-id="dacca-186">**Интерфейс Ивмпфолдермониторсервицес**</span><span class="sxs-lookup"><span data-stu-id="dacca-186">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [<span data-ttu-id="dacca-187">**Интерфейс Ивмплибрари**</span><span class="sxs-lookup"><span data-stu-id="dacca-187">**IWMPLibrary Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [<span data-ttu-id="dacca-188">**Интерфейс Ивмплибрари (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dacca-188">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
-   [<span data-ttu-id="dacca-189">**Интерфейс Ивмплибрарисервицес**</span><span class="sxs-lookup"><span data-stu-id="dacca-189">**IWMPLibraryServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [<span data-ttu-id="dacca-190">**Интерфейс Ивмплибрарисервицес (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dacca-190">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
-   [<span data-ttu-id="dacca-191">**Интерфейс Ивмплибраришарингсервицес**</span><span class="sxs-lookup"><span data-stu-id="dacca-191">**IWMPLibrarySharingServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [<span data-ttu-id="dacca-192">**Интерфейс IWMPMediaCollection2**</span><span class="sxs-lookup"><span data-stu-id="dacca-192">**IWMPMediaCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [<span data-ttu-id="dacca-193">**Интерфейс IWMPMediaCollection2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dacca-193">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
-   [<span data-ttu-id="dacca-194">**Интерфейс Ивмпкуери**</span><span class="sxs-lookup"><span data-stu-id="dacca-194">**IWMPQuery Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [<span data-ttu-id="dacca-195">**Интерфейс Ивмпкуери (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dacca-195">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
-   [<span data-ttu-id="dacca-196">**Интерфейс Ивмпрендерконфиг**</span><span class="sxs-lookup"><span data-stu-id="dacca-196">**IWMPRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [<span data-ttu-id="dacca-197">**Интерфейс IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="dacca-197">**IWMPStringCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [<span data-ttu-id="dacca-198">**Интерфейс IWMPStringCollection2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dacca-198">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
-   [<span data-ttu-id="dacca-199">**Интерфейс IWMPSyncDevice2**</span><span class="sxs-lookup"><span data-stu-id="dacca-199">**IWMPSyncDevice2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [<span data-ttu-id="dacca-200">**Интерфейс Ивмпвидеорендерконфиг**</span><span class="sxs-lookup"><span data-stu-id="dacca-200">**IWMPVideoRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [<span data-ttu-id="dacca-201">**Объект запроса**</span><span class="sxs-lookup"><span data-stu-id="dacca-201">**Query Object**</span></span>](query-object.md)
-   [<span data-ttu-id="dacca-202">**Перечисление Вмпбурнформат**</span><span class="sxs-lookup"><span data-stu-id="dacca-202">**WMPBurnFormat Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [<span data-ttu-id="dacca-203">**Перечисление Вмпбурнстате**</span><span class="sxs-lookup"><span data-stu-id="dacca-203">**WMPBurnState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [<span data-ttu-id="dacca-204">**Перечисление Вмплибраритипе**</span><span class="sxs-lookup"><span data-stu-id="dacca-204">**WMPLibraryType Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [<span data-ttu-id="dacca-205">**Перечисление Вмприпстате**</span><span class="sxs-lookup"><span data-stu-id="dacca-205">**WMPRipState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a><span data-ttu-id="dacca-206">Добавлено для проигрывателя Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="dacca-206">Added for Windows Media Player 12</span></span>

-   [<span data-ttu-id="dacca-207">**Интерфейс Ивмпаудиорендерконфиг**</span><span class="sxs-lookup"><span data-stu-id="dacca-207">**IWMPAudioRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="dacca-208">**Интерфейс IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="dacca-208">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="dacca-209">**Интерфейс IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="dacca-209">**IWMPLibrary2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="dacca-210">**Интерфейс IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="dacca-210">**IWMPSyncDevice3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a><span data-ttu-id="dacca-211">См. также</span><span class="sxs-lookup"><span data-stu-id="dacca-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dacca-212">**Сведения об объектной модели проигрывателя**</span><span class="sxs-lookup"><span data-stu-id="dacca-212">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="dacca-213">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="dacca-213">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




