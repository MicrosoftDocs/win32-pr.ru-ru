---
title: Свойство IMsRdpExtendedSettings Property
description: Содержит именованное свойство.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Свойство свойства службы удаленных рабочих столов
- Свойство свойства службы удаленных рабочих столов, интерфейс Имсрдпекстендедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпекстендедсеттингс, свойство Property
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "103805164"
---
# <a name="imsrdpextendedsettingsproperty-property"></a><span data-ttu-id="4d49b-106">Имсрдпекстендедсеттингс: свойство фильтры:P</span><span class="sxs-lookup"><span data-stu-id="4d49b-106">IMsRdpExtendedSettings::Property property</span></span>

<span data-ttu-id="4d49b-107">Содержит именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="4d49b-107">Contains a named property.</span></span>

<span data-ttu-id="4d49b-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4d49b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d49b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d49b-109">Syntax</span></span>


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a><span data-ttu-id="4d49b-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4d49b-110">Property value</span></span>

<span data-ttu-id="4d49b-111">Значение именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="4d49b-111">The named property value.</span></span>

| <span data-ttu-id="4d49b-112">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="4d49b-112">Property name</span></span> | <span data-ttu-id="4d49b-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4d49b-113">Data type</span></span> | <span data-ttu-id="4d49b-114">Access</span><span class="sxs-lookup"><span data-stu-id="4d49b-114">Access</span></span> | <span data-ttu-id="4d49b-115">Можно изменить после начала подключения</span><span class="sxs-lookup"><span data-stu-id="4d49b-115">Can be changed after connection started</span></span> | <span data-ttu-id="4d49b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4d49b-116">Description</span></span> |
|----------|-----------|--------|-----------------------------------------|-------------|
| <span data-ttu-id="4d49b-117">коннектточилдсессион</span><span class="sxs-lookup"><span data-stu-id="4d49b-117">ConnectToChildSession</span></span> | <span data-ttu-id="4d49b-118">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="4d49b-118">**VT\_BOOL**</span></span> | <span data-ttu-id="4d49b-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4d49b-119">Read/Write</span></span> | <span data-ttu-id="4d49b-120">Да</span><span class="sxs-lookup"><span data-stu-id="4d49b-120">Yes</span></span> | <span data-ttu-id="4d49b-121">Установка этого свойства в **значение true** приводит к тому, что клиентский элемент управления подключается к дочернему сеансу на локальном компьютере, а не на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="4d49b-121">Setting this property to **True** causes the client control to connect to the child session on the local machine instead of a remote server.</span></span> <span data-ttu-id="4d49b-122">Если это свойство имеет значение **true**, подключиться к удаленному серверу невозможно, так как все соединения перенаправляются на localhost.</span><span class="sxs-lookup"><span data-stu-id="4d49b-122">If this property is set to **true**, you cannot connect to a remote server because all connections are redirected to localhost.</span></span> <span data-ttu-id="4d49b-123">Дополнительные сведения о дочерних сеансах см. в разделе [дочерние сеансы](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="4d49b-123">For more information about child sessions, see [Child Sessions](child-sessions.md).</span></span> |
| <span data-ttu-id="4d49b-124">дисаблекредентиалсделегатион</span><span class="sxs-lookup"><span data-stu-id="4d49b-124">DisableCredentialsDelegation</span></span> | <span data-ttu-id="4d49b-125">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="4d49b-125">**VT\_BOOL**</span></span> | <span data-ttu-id="4d49b-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4d49b-126">Read/Write</span></span> | <span data-ttu-id="4d49b-127">Нет</span><span class="sxs-lookup"><span data-stu-id="4d49b-127">No</span></span> | <span data-ttu-id="4d49b-128">Если **значение — true**, учетные данные не отправляются на удаленный сервер.</span><span class="sxs-lookup"><span data-stu-id="4d49b-128">If **True**, credentials are not sent to the remote server.</span></span> |
| <span data-ttu-id="4d49b-129">енаблефрамебуфферредиректион</span><span class="sxs-lookup"><span data-stu-id="4d49b-129">EnableFrameBufferRedirection</span></span> | <span data-ttu-id="4d49b-130">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="4d49b-130">**VT\_BOOL**</span></span> | <span data-ttu-id="4d49b-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4d49b-131">Read/Write</span></span> | <span data-ttu-id="4d49b-132">Нет</span><span class="sxs-lookup"><span data-stu-id="4d49b-132">No</span></span> | <span data-ttu-id="4d49b-133">**Значение true** показывает, что выполняется перенаправление буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="4d49b-133">If **True**, frame buffer redirection is attempted.</span></span> <span data-ttu-id="4d49b-134">Для подключения замыкания на себя (один и тот же компьютер является клиентским и серверным) перенаправление буфера кадров позволяет совместно использовать память для буфера фрейма между сеансами.</span><span class="sxs-lookup"><span data-stu-id="4d49b-134">For a loopback connection (the same computer is both client and server) frame buffer redirection allows the memory for the frame buffer to be shared between the sessions.</span></span> |
| <span data-ttu-id="4d49b-135">енаблехардваремоде</span><span class="sxs-lookup"><span data-stu-id="4d49b-135">EnableHardwareMode</span></span> | <span data-ttu-id="4d49b-136">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="4d49b-136">**VT\_BOOL**</span></span>  | <span data-ttu-id="4d49b-137">Только запись</span><span class="sxs-lookup"><span data-stu-id="4d49b-137">Write Only</span></span> | <span data-ttu-id="4d49b-138">Нет</span><span class="sxs-lookup"><span data-stu-id="4d49b-138">No</span></span> | <span data-ttu-id="4d49b-139">Если задано **значение true**, при помощи аппаратной декодирования осуществляется помощь оборудования.</span><span class="sxs-lookup"><span data-stu-id="4d49b-139">If **True**, hardware assist with graphics decoding is attempted.</span></span> |
| <span data-ttu-id="4d49b-140">игнорекурсорс</span><span class="sxs-lookup"><span data-stu-id="4d49b-140">IgnoreCursors</span></span> | <span data-ttu-id="4d49b-141">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="4d49b-141">**VT\_BOOL**</span></span> | <span data-ttu-id="4d49b-142">Только запись</span><span class="sxs-lookup"><span data-stu-id="4d49b-142">Write Only</span></span> | <span data-ttu-id="4d49b-143">Нет</span><span class="sxs-lookup"><span data-stu-id="4d49b-143">No</span></span> | <span data-ttu-id="4d49b-144">**Значение true** показывает, что курсоры, отправленные удаленным сервером, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="4d49b-144">If **True**, cursors sent by the remote server are ignored.</span></span> |
| <span data-ttu-id="4d49b-145">мануалклипбоардсинценаблед</span><span class="sxs-lookup"><span data-stu-id="4d49b-145">ManualClipboardSyncEnabled</span></span> | <span data-ttu-id="4d49b-146">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="4d49b-146">**VT\_BOOL**</span></span> | <span data-ttu-id="4d49b-147">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4d49b-147">Read/Write</span></span> | <span data-ttu-id="4d49b-148">Да</span><span class="sxs-lookup"><span data-stu-id="4d49b-148">Yes</span></span> | <span data-ttu-id="4d49b-149">Установка этого свойства в **значение true** означает, что локальный и удаленный буфер обмена не будут автоматически синхронизироваться. Вместо этого необходимо использовать интерфейс [**имсрдпклипбоард**](imsrdpclipboard.md) для синхронизации форматов буфера обмена из локального буфера обмена с удаленным буфером обмена и удаленным буфером обмена с локальным буфером обмена.</span><span class="sxs-lookup"><span data-stu-id="4d49b-149">Setting this property to **True** means that the local and remote clipboards will not be automatically kept in sync. Instead the [**IMsRdpClipboard**](imsrdpclipboard.md) interface must be used to sync clipboard formats from the local clipboard to the remote clipboard and the remote clipboard to the local clipboard.</span></span> |
| <span data-ttu-id="4d49b-150">зумлевел</span><span class="sxs-lookup"><span data-stu-id="4d49b-150">ZoomLevel</span></span> | <span data-ttu-id="4d49b-151">\**_VT \_ UI4_*</span><span class="sxs-lookup"><span data-stu-id="4d49b-151">\**_VT\_UI4_*</span></span> | <span data-ttu-id="4d49b-152">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4d49b-152">Read/Write</span></span> | <span data-ttu-id="4d49b-153">Да</span><span class="sxs-lookup"><span data-stu-id="4d49b-153">Yes</span></span> | <span data-ttu-id="4d49b-154">Реализует функцию масштабирования с помощью элемента управления ActiveX RDP.</span><span class="sxs-lookup"><span data-stu-id="4d49b-154">Implements the Zoom feature by using the RDP ActiveX control.</span></span> <span data-ttu-id="4d49b-155">Функция масштабирования доступна в **системном** меню RDP.</span><span class="sxs-lookup"><span data-stu-id="4d49b-155">The Zoom feature is available from the **System** menu of RDP.</span></span> <span data-ttu-id="4d49b-156">Свойство **зумлевел** не действует в режиме RemoteApp и полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="4d49b-156">The **ZoomLevel** property has no effect in RemoteApp mode and full-screen mode.</span></span> <span data-ttu-id="4d49b-157">[**Имсрдпклиентадванцедсеттингс:: смартсизинг**](imsrdpclientadvancedsettings-smartsizing.md) и **зумлевел** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="4d49b-157">[**IMsRdpClientAdvancedSettings::SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) and **ZoomLevel** are mutually exclusive.</span></span> |

## <a name="requirements"></a><span data-ttu-id="4d49b-158">Требования</span><span class="sxs-lookup"><span data-stu-id="4d49b-158">Requirements</span></span>



| <span data-ttu-id="4d49b-159">Требование</span><span class="sxs-lookup"><span data-stu-id="4d49b-159">Requirement</span></span> | <span data-ttu-id="4d49b-160">Значение</span><span class="sxs-lookup"><span data-stu-id="4d49b-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d49b-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d49b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="4d49b-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4d49b-162">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="4d49b-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d49b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="4d49b-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d49b-164">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4d49b-165">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4d49b-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d49b-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d49b-166"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="4d49b-167">DLL</span><span class="sxs-lookup"><span data-stu-id="4d49b-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d49b-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d49b-168"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="4d49b-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="4d49b-169">CLSID</span></span><br/>                    | <span data-ttu-id="4d49b-170">\_MSRDPCLIENT7NOTSAFEFORSCRIPTING CLSID определен как 54d38bf7-b1ef-4479-9674-1bd6ea465258</span><span class="sxs-lookup"><span data-stu-id="4d49b-170">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54d38bf7-b1ef-4479-9674-1bd6ea465258</span></span><br/> <span data-ttu-id="4d49b-171">\_MSRDPCLIENT8NOTSAFEFORSCRIPTING CLSID определен как A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="4d49b-171">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="4d49b-172">\_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="4d49b-172">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="4d49b-173">IID</span><span class="sxs-lookup"><span data-stu-id="4d49b-173">IID</span></span><br/>                      | <span data-ttu-id="4d49b-174">IID \_ имсрдпекстендедсеттингс определен как 302D8188-0052-4807-806A-362B628F9AC5</span><span class="sxs-lookup"><span data-stu-id="4d49b-174">IID\_IMsRdpExtendedSettings is defined as 302D8188-0052-4807-806A-362B628F9AC5</span></span><br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a><span data-ttu-id="4d49b-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d49b-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d49b-176">**имсрдпекстендедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="4d49b-176">**IMsRdpExtendedSettings**</span></span>](imsrdpextendedsettings.md)
</dt> </dl>

 

 





