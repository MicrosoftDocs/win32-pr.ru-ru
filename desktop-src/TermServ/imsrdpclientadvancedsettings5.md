---
title: Интерфейс IMsRdpClientAdvancedSettings5
description: Управляет дополнительными параметрами клиента. Является производным от интерфейса IMsRdpClientAdvancedSettings4.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e37eb28c1fb7a272291c44661c52ec3548708b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681888"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a><span data-ttu-id="0fef2-106">Интерфейс IMsRdpClientAdvancedSettings5</span><span class="sxs-lookup"><span data-stu-id="0fef2-106">IMsRdpClientAdvancedSettings5 interface</span></span>

<span data-ttu-id="0fef2-107">Управляет дополнительными параметрами клиента.</span><span class="sxs-lookup"><span data-stu-id="0fef2-107">Manages advanced client settings.</span></span> <span data-ttu-id="0fef2-108">Является производным от интерфейса [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="0fef2-108">Derives from the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="0fef2-109">Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="0fef2-109">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="0fef2-110">Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings5** в **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="0fef2-110">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings5** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="0fef2-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="0fef2-111">Members</span></span>

<span data-ttu-id="0fef2-112">Интерфейс **IMsRdpClientAdvancedSettings5** наследует от [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span><span class="sxs-lookup"><span data-stu-id="0fef2-112">The **IMsRdpClientAdvancedSettings5** interface inherits from [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span></span> <span data-ttu-id="0fef2-113">**IMsRdpClientAdvancedSettings5** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0fef2-113">**IMsRdpClientAdvancedSettings5** also has these types of members:</span></span>

-   [<span data-ttu-id="0fef2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="0fef2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fef2-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="0fef2-115">Properties</span></span>

<span data-ttu-id="0fef2-116">Интерфейс **IMsRdpClientAdvancedSettings5** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0fef2-116">The **IMsRdpClientAdvancedSettings5** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0fef2-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="0fef2-117">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0fef2-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="0fef2-118">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0fef2-119">Описание</span><span class="sxs-lookup"><span data-stu-id="0fef2-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0fef2-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>аудиоредиректионмоде</strong></a></span><span class="sxs-lookup"><span data-stu-id="0fef2-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0fef2-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-122">Режим перенаправления звука.</span><span class="sxs-lookup"><span data-stu-id="0fef2-122">The audio redirection mode.</span></span> <span data-ttu-id="0fef2-123">Свойство <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>аудиоредиректионмоде</strong></a> имеет следующие возможные значения.</span><span class="sxs-lookup"><span data-stu-id="0fef2-123">The <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> property has the following possible values.</span></span><br/><span data-ttu-id="0fef2-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (перенаправление звука включено, а параметр перенаправления — &quot; на этот компьютер) &quot; .</span><span class="sxs-lookup"><span data-stu-id="0fef2-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (Audio redirection is enabled and the option for redirection is &quot;Bring to this computer&quot;.</span></span> <span data-ttu-id="0fef2-125">Это режим по умолчанию.)</span><span class="sxs-lookup"><span data-stu-id="0fef2-125">This is the default mode.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="0fef2-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (перенаправление звука включено, а параметр — &quot; оставить на удаленном компьютере) &quot; .</span><span class="sxs-lookup"><span data-stu-id="0fef2-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (Audio redirection is enabled and the option is &quot;Leave at remote computer&quot;.</span></span> <span data-ttu-id="0fef2-127">&quot;Параметр оставить на удаленном компьютере &quot; поддерживается только при удаленном подключении к главному компьютеру под управлением Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0fef2-127">The &quot;Leave at remote computer&quot; option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="0fef2-128">Если подключение установлено к главному компьютеру под Windows Server 2008, параметр &quot; оставить на удаленном компьютере &quot; изменен на не &quot; воспроизводить &quot; .)</span><span class="sxs-lookup"><span data-stu-id="0fef2-128">If the connection is to a host computer that is running Windows Server 2008, the option &quot;Leave at remote computer&quot; is changed to &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="0fef2-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (перенаправление звука включено и режим не &quot; воспроизводится &quot; ).</span><span class="sxs-lookup"><span data-stu-id="0fef2-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (Audio redirection is enabled and the mode is &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="0fef2-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="0fef2-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0fef2-131">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-132">Задает размер файла виртуального кэша для точечных рисунков 32 бит на пиксель (бит в пикселах).</span><span class="sxs-lookup"><span data-stu-id="0fef2-132">Specifies the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span> <span data-ttu-id="0fef2-133">Максимальное значение — 48 МБ.</span><span class="sxs-lookup"><span data-stu-id="0fef2-133">The maximum value is 48 megabytes (MB).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0fef2-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>коннектионбаршовпинбуттон</strong></a></span><span class="sxs-lookup"><span data-stu-id="0fef2-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0fef2-135">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-136">Указывает, должна ли отображаться кнопка закрепить на панели подключения.</span><span class="sxs-lookup"><span data-stu-id="0fef2-136">Specifies whether the pin button should be shown on the connection bar.</span></span> <span data-ttu-id="0fef2-137">По умолчанию значение равно <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="0fef2-137">By default, the value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="0fef2-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>публикмоде</strong></a></span><span class="sxs-lookup"><span data-stu-id="0fef2-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-139">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0fef2-139">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-140">Указывает, следует ли включить или отключить общедоступный режим.</span><span class="sxs-lookup"><span data-stu-id="0fef2-140">Specifies whether public mode should be enabled or disabled.</span></span> <span data-ttu-id="0fef2-141">По умолчанию общедоступный режим имеет значение <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="0fef2-141">By default, public mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0fef2-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>редиректклипбоард</strong></a></span><span class="sxs-lookup"><span data-stu-id="0fef2-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-143">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0fef2-143">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-144">Указывает, следует ли включить или отключить перенаправление буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="0fef2-144">Specifies whether clipboard redirection should be enabled or disabled.</span></span> <span data-ttu-id="0fef2-145">По умолчанию режим перенаправления буфера обмена имеет значение <strong>true</strong> (включено).</span><span class="sxs-lookup"><span data-stu-id="0fef2-145">By default, clipboard redirection mode is set to <strong>TRUE</strong> (enabled).</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="0fef2-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>редиректдевицес</strong></a></span><span class="sxs-lookup"><span data-stu-id="0fef2-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-147">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0fef2-147">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-148">Указывает, должны ли перенаправленные устройства быть включены или отключены.</span><span class="sxs-lookup"><span data-stu-id="0fef2-148">Specifies whether redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="0fef2-149">По умолчанию для параметра режим перенаправленных устройств задано значение <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="0fef2-149">By default, redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0fef2-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>редиректпосдевицес</strong></a></span><span class="sxs-lookup"><span data-stu-id="0fef2-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-151">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0fef2-151">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0fef2-152">Указывает, следует ли включить или отключить перенаправленные устройства точки обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0fef2-152">Specifies whether Point of Service redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="0fef2-153">По умолчанию режим перенаправленных устройств точки обслуживания имеет значение <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="0fef2-153">By default, Point of Service redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0fef2-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0fef2-154">Remarks</span></span>

<span data-ttu-id="0fef2-155">Этот интерфейс расширен следующими интерфейсами, при этом каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="0fef2-155">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="0fef2-156">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0fef2-156">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="0fef2-157">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0fef2-157">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="0fef2-158">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0fef2-158">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a><span data-ttu-id="0fef2-159">Требования</span><span class="sxs-lookup"><span data-stu-id="0fef2-159">Requirements</span></span>



| <span data-ttu-id="0fef2-160">Требование</span><span class="sxs-lookup"><span data-stu-id="0fef2-160">Requirement</span></span> | <span data-ttu-id="0fef2-161">Значение</span><span class="sxs-lookup"><span data-stu-id="0fef2-161">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fef2-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0fef2-162">Minimum supported client</span></span><br/> | <span data-ttu-id="0fef2-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fef2-163">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="0fef2-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0fef2-164">Minimum supported server</span></span><br/> | <span data-ttu-id="0fef2-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fef2-165">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="0fef2-166">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0fef2-166">Type library</span></span><br/>             | <dl> <span data-ttu-id="0fef2-167"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fef2-167"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0fef2-168">DLL</span><span class="sxs-lookup"><span data-stu-id="0fef2-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fef2-169"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fef2-169"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0fef2-170">IID</span><span class="sxs-lookup"><span data-stu-id="0fef2-170">IID</span></span><br/>                      | <span data-ttu-id="0fef2-171">IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="0fef2-171">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fef2-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fef2-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fef2-173">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0fef2-173">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0fef2-174">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0fef2-174">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="0fef2-175">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0fef2-175">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0fef2-176">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="0fef2-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0fef2-177">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="0fef2-177">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0fef2-178">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="0fef2-178">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

