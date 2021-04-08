---
title: IMsRdpClientAdvancedSettings4 Аусентикатионлевел, свойство
description: Указывает уровень проверки подлинности, используемый для соединения.
ms.assetid: 09ff1508-f13d-4bb0-8458-6f5a5e099bae
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Аусентикатионлевел
- Службы удаленных рабочих столов свойства Аусентикатионлевел, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Аусентикатионлевел
- Службы удаленных рабочих столов свойства Аусентикатионлевел, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Аусентикатионлевел
- Службы удаленных рабочих столов свойства Аусентикатионлевел, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Аусентикатионлевел
- Службы удаленных рабочих столов свойства Аусентикатионлевел, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Аусентикатионлевел
- Службы удаленных рабочих столов свойства Аусентикатионлевел, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Аусентикатионлевел
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4.AuthenticationLevel
- IMsRdpClientAdvancedSettings4.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings4.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.AuthenticationLevel
- IMsRdpClientAdvancedSettings5.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.AuthenticationLevel
- IMsRdpClientAdvancedSettings6.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.AuthenticationLevel
- IMsRdpClientAdvancedSettings7.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.AuthenticationLevel
- IMsRdpClientAdvancedSettings8.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.put_AuthenticationLevel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c748416650ec7e6ec3d26fe6236a254eb012d67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891821"
---
# <a name="imsrdpclientadvancedsettings4authenticationlevel-property"></a><span data-ttu-id="a86d6-114">Свойство IMsRdpClientAdvancedSettings4:: Аусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="a86d6-114">IMsRdpClientAdvancedSettings4::AuthenticationLevel property</span></span>

<span data-ttu-id="a86d6-115">Указывает уровень проверки подлинности, используемый для соединения.</span><span class="sxs-lookup"><span data-stu-id="a86d6-115">Specifies the authentication level to use for the connection.</span></span>

<span data-ttu-id="a86d6-116">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a86d6-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a86d6-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a86d6-117">Syntax</span></span>


```C++
HRESULT put_AuthenticationLevel(
  [in]  UINT uiAuthLevel
);

HRESULT get_AuthenticationLevel(
  [out] UINT *puiAuthLevel
);
```



## <a name="property-value"></a><span data-ttu-id="a86d6-118">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a86d6-118">Property value</span></span>

<span data-ttu-id="a86d6-119">Значение свойства **аусентикатионлевел** .</span><span class="sxs-lookup"><span data-stu-id="a86d6-119">The value of the **AuthenticationLevel** property.</span></span>

<dt>

<span data-ttu-id="a86d6-120">0</span><span class="sxs-lookup"><span data-stu-id="a86d6-120">0</span></span>
</dt> <dd>

<span data-ttu-id="a86d6-121">Нет проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="a86d6-121">No authentication of the server.</span></span>

</dd> <dt>

<span data-ttu-id="a86d6-122">1</span><span class="sxs-lookup"><span data-stu-id="a86d6-122">1</span></span>
</dt> <dd>

<span data-ttu-id="a86d6-123">Для продолжения подключения требуется проверка подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="a86d6-123">Server authentication is required and must complete successfully for the connection to proceed.</span></span>

</dd> <dt>

<span data-ttu-id="a86d6-124">2</span><span class="sxs-lookup"><span data-stu-id="a86d6-124">2</span></span>
</dt> <dd>

<span data-ttu-id="a86d6-125">Попытайтесь выполнить проверку подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="a86d6-125">Attempt authentication of the server.</span></span> <span data-ttu-id="a86d6-126">Если проверка подлинности завершается неудачно, пользователю будет предложено отменить подключение или продолжить работу без проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="a86d6-126">If authentication fails, the user will be prompted with the option to cancel the connection or to proceed without server authentication.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="a86d6-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a86d6-127">Error codes</span></span>

<span data-ttu-id="a86d6-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="a86d6-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a86d6-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a86d6-129">Remarks</span></span>

<span data-ttu-id="a86d6-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a86d6-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a86d6-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a86d6-131">Requirements</span></span>



| <span data-ttu-id="a86d6-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a86d6-132">Requirement</span></span> | <span data-ttu-id="a86d6-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a86d6-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a86d6-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a86d6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a86d6-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a86d6-135">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a86d6-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a86d6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a86d6-137">Windows Server 2008, Windows Server 2008 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="a86d6-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="a86d6-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a86d6-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="a86d6-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a86d6-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a86d6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a86d6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a86d6-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a86d6-141"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a86d6-142">IID</span><span class="sxs-lookup"><span data-stu-id="a86d6-142">IID</span></span><br/>                      | <span data-ttu-id="a86d6-143">IID \_ IMsRdpClientAdvancedSettings4 определяется как FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="a86d6-143">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a86d6-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a86d6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a86d6-145">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a86d6-145">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a86d6-146">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a86d6-146">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a86d6-147">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a86d6-147">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a86d6-148">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a86d6-148">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a86d6-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a86d6-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> </dl>

 

 





