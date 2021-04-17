---
title: Имстсксекуредсеттингс, свойство полноэкранного режима
description: Задает полноэкранное состояние клиентского элемента управления.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства во весь экран
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс Имстсксекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имстсксекуредсеттингс, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс Имсрдпклиентсекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс, свойство "во весь экран"
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672833"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a><span data-ttu-id="cd481-108">Свойство Имстсксекуредсеттингс:: полноэкранного режима</span><span class="sxs-lookup"><span data-stu-id="cd481-108">IMsTscSecuredSettings::Fullscreen property</span></span>

<span data-ttu-id="cd481-109">Задает полноэкранное состояние клиентского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cd481-109">Specifies the full-screen state of the client control.</span></span>

<span data-ttu-id="cd481-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="cd481-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd481-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd481-111">Syntax</span></span>


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="cd481-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cd481-112">Property value</span></span>

<span data-ttu-id="cd481-113">Задайте для этого параметра **значение true** , если элемент управления должен использовать полноэкранный режим, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cd481-113">Set this parameter to **TRUE** if the control should use full-screen mode and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cd481-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="cd481-114">Error codes</span></span>

<span data-ttu-id="cd481-115">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="cd481-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd481-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd481-116">Remarks</span></span>

<span data-ttu-id="cd481-117">Дополнительные сведения об этом методе см. в разделе [предоставление для безопасности клиента RDP](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="cd481-117">For more information about this method, see [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="cd481-118">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cd481-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

<span data-ttu-id="cd481-119">Обратите внимание, что несмотря на то, что использование этого свойства ограничено разрешенными зонами безопасности URL-адресов Internet Explorer, пользователь всегда может перейти в полноэкранный режим после установки подключения, нажав [сочетание клавиш в полноэкранном режиме (](terminal-services-shortcut-keys.md) Ctrl + Alt + Break).</span><span class="sxs-lookup"><span data-stu-id="cd481-119">Note that although the use of this property is restricted to the allowed Internet Explorer URL security zones, a user can always change to full-screen mode after the connection has been established by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="cd481-120">Этот метод может быть вызван во время установки клиентского соединения.</span><span class="sxs-lookup"><span data-stu-id="cd481-120">This method can be called while the client connection is established.</span></span>

<span data-ttu-id="cd481-121">Необходимо вызвать метод [**IMsRdpClientNonScriptable3::p UT \_ коннектионбартекст**](imsrdpclientnonscriptable3-connectionbartext.md) перед вызовом метода **имстсксекуредсеттингс::p UT \_** , а также метода [**имсрдпклиент::p UT \_**](imsrdpclient-fullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="cd481-121">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the **IMsTscSecuredSettings::put\_Fullscreen** method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd481-122">Требования</span><span class="sxs-lookup"><span data-stu-id="cd481-122">Requirements</span></span>



| <span data-ttu-id="cd481-123">Требование</span><span class="sxs-lookup"><span data-stu-id="cd481-123">Requirement</span></span> | <span data-ttu-id="cd481-124">Значение</span><span class="sxs-lookup"><span data-stu-id="cd481-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd481-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd481-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cd481-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd481-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="cd481-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd481-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cd481-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd481-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="cd481-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cd481-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd481-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd481-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="cd481-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cd481-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd481-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd481-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="cd481-133">IID</span><span class="sxs-lookup"><span data-stu-id="cd481-133">IID</span></span><br/>                      | <span data-ttu-id="cd481-134">IID \_ имстсксекуредсеттингс определен как c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="cd481-134">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd481-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd481-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd481-136">**имсрдпклиентсекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="cd481-136">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="cd481-137">**имстсксекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="cd481-137">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





