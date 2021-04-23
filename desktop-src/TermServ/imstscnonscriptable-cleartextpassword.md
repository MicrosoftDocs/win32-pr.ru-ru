---
title: Имстскнонскриптабле Клеартекстпассворд, свойство
description: Задает удаленный рабочий стол пароля элемента управления ActiveX в текстовом формате.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс Имстскнонскриптабле
- Службы удаленных рабочих столов интерфейса Имстскнонскриптабле, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс Имсрдпклиентнонскриптабле
- Службы удаленных рабочих столов интерфейса Имсрдпклиентнонскриптабле, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientNonScriptable2
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable2, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Клеартекстпассворд
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803796"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a><span data-ttu-id="490cf-124">Свойство Имстскнонскриптабле:: Клеартекстпассворд</span><span class="sxs-lookup"><span data-stu-id="490cf-124">IMsTscNonScriptable::ClearTextPassword property</span></span>

<span data-ttu-id="490cf-125">Задает удаленный рабочий стол пароля элемента управления ActiveX в текстовом формате.</span><span class="sxs-lookup"><span data-stu-id="490cf-125">Sets the Remote Desktop ActiveX control password in plaintext format.</span></span>

<span data-ttu-id="490cf-126">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="490cf-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="490cf-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="490cf-127">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a><span data-ttu-id="490cf-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="490cf-128">Property value</span></span>

<span data-ttu-id="490cf-129">Пароль, используемый для подключения, указанный в текстовом формате.</span><span class="sxs-lookup"><span data-stu-id="490cf-129">The password to be used to connect, specified in plaintext format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="490cf-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="490cf-130">Error codes</span></span>

<span data-ttu-id="490cf-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="490cf-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="490cf-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="490cf-132">Remarks</span></span>

<span data-ttu-id="490cf-133">Пароль передается на сервер в безопасно зашифрованном канале связи RDP.</span><span class="sxs-lookup"><span data-stu-id="490cf-133">The password is passed to the server in the safely encrypted RDP communications channel.</span></span> <span data-ttu-id="490cf-134">После установки пароля в виде открытого текста он не может быть получен в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="490cf-134">After a plaintext password is set, it cannot be retrieved in plaintext format.</span></span>

<span data-ttu-id="490cf-135">Свойство **клеартекстпассворд** может быть задано, только если удаленный рабочий стол элемент управления ActiveX не находится в состоянии Connected.</span><span class="sxs-lookup"><span data-stu-id="490cf-135">The **ClearTextPassword** property can only be set when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="490cf-136">Установка этого свойства завершается ошибкой, если элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="490cf-136">Setting this property fails if the control is connected.</span></span> <span data-ttu-id="490cf-137">Чтобы проверить состояние Connected, извлеките свойство [**имстскакс:: Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="490cf-137">To check for the connected state, retrieve the [**IMsTscAx::Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="490cf-138">Этот метод также можно вызвать для установки пароля в виде открытого текста перед его преобразованием в переносимый закодированный пароль или в двоичный (непреобразуемый) пароль.</span><span class="sxs-lookup"><span data-stu-id="490cf-138">You can also call this method to set a plaintext password before converting it to either a portable encoded password or to a binary (nonportable) encoded password.</span></span> <span data-ttu-id="490cf-139">Обратите внимание, что зашифрованные пароли не должны считаться безопасными.</span><span class="sxs-lookup"><span data-stu-id="490cf-139">Note however that encoded passwords should not be considered securely encrypted.</span></span>

<span data-ttu-id="490cf-140">При первом вызове этого метода для задания пароля в формате обычного текста можно преобразовать пароль в формат Encoded.</span><span class="sxs-lookup"><span data-stu-id="490cf-140">If you first call this method to set a password in plaintext format, you can then convert the password to encoded format.</span></span>

<span data-ttu-id="490cf-141">**Преобразование пароля в формате обычного текста в закодированный формат**</span><span class="sxs-lookup"><span data-stu-id="490cf-141">**To convert a plaintext password to encoded format**</span></span>

1.  <span data-ttu-id="490cf-142">Задайте пароль в формате обычного текста в свойстве **клеартекстпассворд** .</span><span class="sxs-lookup"><span data-stu-id="490cf-142">Set the password in plaintext format in the **ClearTextPassword** property.</span></span>
2.  <span data-ttu-id="490cf-143">Чтобы получить пароль в двоичном (незакодированном) формате в кодировке, извлеките свойство [**бинарипассворд**](imstscnonscriptable-binarypassword.md) и свойства [**бинарисалт**](imstscnonscriptable-binarysalt.md) .</span><span class="sxs-lookup"><span data-stu-id="490cf-143">To retrieve the password in binary (nonportable) encoded format, retrieve the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) property and the [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties.</span></span> <span data-ttu-id="490cf-144">Для задания пароля в двоичном кодированном формате требуется как часть закодированного пароля, так и часть соли.</span><span class="sxs-lookup"><span data-stu-id="490cf-144">Both the encoded password part and the salt part are required to set a password in binary encoded format.</span></span>
3.  <span data-ttu-id="490cf-145">Чтобы получить пароль в переносимом кодированном формате, извлеките метод [**портаблепассворд**](imstscnonscriptable-portablepassword.md) и свойства [**портаблесалт**](imstscnonscriptable-portablesalt.md) .</span><span class="sxs-lookup"><span data-stu-id="490cf-145">To retrieve the password in portable encoded format, retrieve the [**PortablePassword**](imstscnonscriptable-portablepassword.md) method and the [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="490cf-146">Обе части необходимы для установки пароля в переносимом кодированном формате.</span><span class="sxs-lookup"><span data-stu-id="490cf-146">Both parts are required to set a password in portable encoded format.</span></span>

<span data-ttu-id="490cf-147">После выполнения предыдущих трех шагов можно задать пароль в закодированном формате, задав свойства [**бинарипассворд**](imstscnonscriptable-binarypassword.md) и [**бинарисалт**](imstscnonscriptable-binarysalt.md) , а также свойства [**портаблепассворд**](imstscnonscriptable-portablepassword.md) и [**портаблесалт**](imstscnonscriptable-portablesalt.md) .</span><span class="sxs-lookup"><span data-stu-id="490cf-147">After following the preceding three steps, you can set the password in encoded format by setting the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) and [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties, or [**PortablePassword**](imstscnonscriptable-portablepassword.md) and [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="490cf-148">Требуются обе части.</span><span class="sxs-lookup"><span data-stu-id="490cf-148">Both parts are required.</span></span>

<span data-ttu-id="490cf-149">Чтобы включить автоматический вход в систему, необходимо также задать свойства [**username**](imstscax-username.md) и [**domain**](imstscax-domain.md) .</span><span class="sxs-lookup"><span data-stu-id="490cf-149">To enable automatic logon, you must also set the [**UserName**](imstscax-username.md) and [**Domain**](imstscax-domain.md) properties.</span></span> <span data-ttu-id="490cf-150">Если пароль не проходит проверку подлинности пользователя, на сервере отображается диалоговое окно входа в Windows, в котором пользователю предлагается ввести пароль.</span><span class="sxs-lookup"><span data-stu-id="490cf-150">If the password fails to authenticate the user, the Windows Logon dialog box is displayed at the server to prompt the user for the password.</span></span>

<span data-ttu-id="490cf-151">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="490cf-151">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="490cf-152">Требования</span><span class="sxs-lookup"><span data-stu-id="490cf-152">Requirements</span></span>



| <span data-ttu-id="490cf-153">Требование</span><span class="sxs-lookup"><span data-stu-id="490cf-153">Requirement</span></span> | <span data-ttu-id="490cf-154">Значение</span><span class="sxs-lookup"><span data-stu-id="490cf-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="490cf-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="490cf-155">Minimum supported client</span></span><br/> | <span data-ttu-id="490cf-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="490cf-156">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="490cf-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="490cf-157">Minimum supported server</span></span><br/> | <span data-ttu-id="490cf-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="490cf-158">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="490cf-159">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="490cf-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="490cf-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="490cf-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="490cf-161">DLL</span><span class="sxs-lookup"><span data-stu-id="490cf-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="490cf-162"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="490cf-162"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="490cf-163">IID</span><span class="sxs-lookup"><span data-stu-id="490cf-163">IID</span></span><br/>                      | <span data-ttu-id="490cf-164">IID \_ имстскнонскриптабле определен как c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="490cf-164">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="490cf-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="490cf-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="490cf-166">**имсрдпклиентнонскриптабле**</span><span class="sxs-lookup"><span data-stu-id="490cf-166">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="490cf-167">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="490cf-167">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="490cf-168">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="490cf-168">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="490cf-169">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="490cf-169">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="490cf-170">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="490cf-170">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="490cf-171">**имстскнонскриптабле**</span><span class="sxs-lookup"><span data-stu-id="490cf-171">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





