---
title: Интерфейс Имстскадванцедсеттингс
description: Содержит методы для получения и задания свойств, обеспечивающих кэширование растровых изображений, сжатие, а также перенаправление принтера и буфера обмена.
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс, описание
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4d55df30c940ecc5a5515f13c05a285507499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672665"
---
# <a name="imstscadvancedsettings-interface"></a><span data-ttu-id="68361-105">Интерфейс Имстскадванцедсеттингс</span><span class="sxs-lookup"><span data-stu-id="68361-105">IMsTscAdvancedSettings interface</span></span>

<span data-ttu-id="68361-106">Содержит методы для получения и задания свойств, обеспечивающих кэширование растровых изображений, сжатие, а также перенаправление принтера и буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="68361-106">Includes methods to retrieve and set properties that enable bitmap caching, compression, and printer and clipboard redirection.</span></span> <span data-ttu-id="68361-107">Можно также указать имена клиентских библиотек DLL для виртуальных каналов.</span><span class="sxs-lookup"><span data-stu-id="68361-107">You can also specify names of virtual channel client DLLs.</span></span>

<span data-ttu-id="68361-108">Экземпляр этого интерфейса можно получить с помощью свойства [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="68361-108">You obtain an instance of this interface by using the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="68361-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="68361-109">Members</span></span>

<span data-ttu-id="68361-110">Интерфейс **имстскадванцедсеттингс** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="68361-110">The **IMsTscAdvancedSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="68361-111">**Имстскадванцедсеттингс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="68361-111">**IMsTscAdvancedSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="68361-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="68361-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68361-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="68361-113">Properties</span></span>

<span data-ttu-id="68361-114">Интерфейс **имстскадванцедсеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="68361-114">The **IMsTscAdvancedSettings** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="68361-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="68361-115">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="68361-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="68361-116">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="68361-117">Описание</span><span class="sxs-lookup"><span data-stu-id="68361-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="68361-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>алловбаккграундинпут</strong></a></span><span class="sxs-lookup"><span data-stu-id="68361-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="68361-119">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-120">Указывает, включен ли режим фонового ввода.</span><span class="sxs-lookup"><span data-stu-id="68361-120">Specifies whether background input mode is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="68361-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>битмапперистенце</strong></a></span><span class="sxs-lookup"><span data-stu-id="68361-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="68361-122">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-123">Указывает, включено ли кэширование растровых изображений.</span><span class="sxs-lookup"><span data-stu-id="68361-123">Specifies whether bitmap caching is enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="68361-124">Орфографическая ошибка в имени свойства находится в выпущенной версии элемента управления.</span><span class="sxs-lookup"><span data-stu-id="68361-124">The spelling error in the name of the property is in the released version of the control.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="68361-125"><a href="imstscadvancedsettings-compress.md"><strong>Повторно</strong></a></span><span class="sxs-lookup"><span data-stu-id="68361-125"><a href="imstscadvancedsettings-compress.md"><strong>Compress</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="68361-126">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-127">Указывает, включено ли сжатие.</span><span class="sxs-lookup"><span data-stu-id="68361-127">Specifies whether compression is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="68361-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>контаинерхандледфуллскрин</strong></a></span><span class="sxs-lookup"><span data-stu-id="68361-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="68361-129">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-130">Указывает, включен ли полноэкранный режим, обрабатываемый контейнером.</span><span class="sxs-lookup"><span data-stu-id="68361-130">Specifies whether the container-handled full-screen mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="68361-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>дисаблердпдр</strong></a></span><span class="sxs-lookup"><span data-stu-id="68361-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="68361-132">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-133">Указывает, включено ли перенаправление принтеров и буферов обмена.</span><span class="sxs-lookup"><span data-stu-id="68361-133">Specifies whether printer and clipboard redirection is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="68361-134"><a href="imstscadvancedsettings-iconfile.md"><strong>иконфиле</strong></a></span><span class="sxs-lookup"><span data-stu-id="68361-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-135">Только на запись</span><span class="sxs-lookup"><span data-stu-id="68361-135">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-136">Указывает имя файла, содержащего данные значков, которые будут доступны при отображении клиента в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="68361-136">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="68361-137"><a href="imstscadvancedsettings-iconindex.md"><strong>икониндекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="68361-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-138">Только на запись</span><span class="sxs-lookup"><span data-stu-id="68361-138">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-139">Задает индекс значка в текущем файле значка.</span><span class="sxs-lookup"><span data-stu-id="68361-139">Specifies the index of the icon within the current icon file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="68361-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>кэйбоардлайаутстр</strong></a></span><span class="sxs-lookup"><span data-stu-id="68361-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-141">Только на запись</span><span class="sxs-lookup"><span data-stu-id="68361-141">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-142">Задает имя активного идентификатора языка ввода (прежнее название раскладки клавиатуры), используемого для соединения.</span><span class="sxs-lookup"><span data-stu-id="68361-142">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="68361-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>плугиндллс</strong></a></span><span class="sxs-lookup"><span data-stu-id="68361-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-144">Только на запись</span><span class="sxs-lookup"><span data-stu-id="68361-144">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="68361-145">Указывает имена клиентских DLL-библиотек виртуальных каналов для загрузки.</span><span class="sxs-lookup"><span data-stu-id="68361-145">Specifies the names of virtual channel client DLLs to be loaded.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="68361-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68361-146">Remarks</span></span>

<span data-ttu-id="68361-147">Этот интерфейс расширен следующими интерфейсами, при этом каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="68361-147">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="68361-148">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="68361-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
-   [<span data-ttu-id="68361-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="68361-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
-   [<span data-ttu-id="68361-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="68361-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
-   [<span data-ttu-id="68361-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="68361-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="68361-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="68361-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="68361-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="68361-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="68361-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="68361-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="68361-155">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="68361-155">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68361-156">Требования</span><span class="sxs-lookup"><span data-stu-id="68361-156">Requirements</span></span>



| <span data-ttu-id="68361-157">Требование</span><span class="sxs-lookup"><span data-stu-id="68361-157">Requirement</span></span> | <span data-ttu-id="68361-158">Значение</span><span class="sxs-lookup"><span data-stu-id="68361-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="68361-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68361-159">Minimum supported client</span></span><br/> | <span data-ttu-id="68361-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68361-160">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="68361-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68361-161">Minimum supported server</span></span><br/> | <span data-ttu-id="68361-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68361-162">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="68361-163">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="68361-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="68361-164"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68361-164"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="68361-165">DLL</span><span class="sxs-lookup"><span data-stu-id="68361-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68361-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68361-166"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="68361-167">IID</span><span class="sxs-lookup"><span data-stu-id="68361-167">IID</span></span><br/>                      | <span data-ttu-id="68361-168">IID \_ имстскадванцедсеттингс определен как 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="68361-168">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68361-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68361-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68361-170">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="68361-170">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="68361-171">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="68361-171">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

