---
title: Имстскнонскриптабле Ресетпассворд, метод
description: Сбрасывает все состояния паролей в удаленный рабочий стол элементе управления ActiveX.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ресетпассворд
- Службы удаленных рабочих столов метода Ресетпассворд, интерфейс Имстскнонскриптабле
- Службы удаленных рабочих столов интерфейса Имстскнонскриптабле, метод Ресетпассворд
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492774"
---
# <a name="imstscnonscriptableresetpassword-method"></a><span data-ttu-id="9fe0c-106">Метод Имстскнонскриптабле:: Ресетпассворд</span><span class="sxs-lookup"><span data-stu-id="9fe0c-106">IMsTscNonScriptable::ResetPassword method</span></span>

<span data-ttu-id="9fe0c-107">Сбрасывает все состояния паролей в удаленный рабочий стол элементе управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-107">Resets all password states in the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="9fe0c-108">Этот метод можно вызвать для очистки паролей, хранящихся в одном из трех поддерживаемых форматов: обычный текст, переносимая кодировка или двоичный (неподдерживающий) формат.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-108">You can call this method to clear passwords that are stored in any one of the three supported formats: plaintext, portable encoded, or binary (nonportable) encoded.</span></span> <span data-ttu-id="9fe0c-109">Обратите внимание, что зашифрованные пароли не следует считать безопасными.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-109">Note that encoded passwords should not be considered securely encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe0c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fe0c-110">Syntax</span></span>


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a><span data-ttu-id="9fe0c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fe0c-111">Parameters</span></span>

<span data-ttu-id="9fe0c-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9fe0c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fe0c-113">Return value</span></span>

<span data-ttu-id="9fe0c-114">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="9fe0c-114">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fe0c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fe0c-115">Remarks</span></span>

<span data-ttu-id="9fe0c-116">Этот метод можно вызвать для сброса пароля элемента управления после отключения.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-116">You can call this method to reset the control's password after disconnecting.</span></span> <span data-ttu-id="9fe0c-117">Это гарантирует, что при последующих соединениях, использующих один и тот же экземпляр элемента управления, не будет автоматически входить в систему с установленным ранее паролем.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-117">This ensures that subsequent connections that use the same instance of the control do not automatically log on with a previously set password.</span></span>

<span data-ttu-id="9fe0c-118">Этот метод можно вызывать только в том случае, если удаленный рабочий стол элемент управления ActiveX не находится в состоянии Connected.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-118">You can only call this method when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="9fe0c-119">Этот метод возвращает **E \_ Fail** , если он вызывается при соединении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-119">This method returns **E\_FAIL** if called when the control is connected.</span></span> <span data-ttu-id="9fe0c-120">Чтобы проверить состояние Connected, вызовите метод [**Get \_ Connected**](imstscax-connected.md) через интерфейс [**имстскакс**](imstscax-interface.md) или один из интерфейсов, наследующих от него.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-120">To check for the connected state, call the [**get\_Connected**](imstscax-connected.md) method through the [**IMsTscAx**](imstscax-interface.md) interface or one of the interfaces that inherits from it.</span></span>

<span data-ttu-id="9fe0c-121">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9fe0c-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe0c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9fe0c-122">Requirements</span></span>



| <span data-ttu-id="9fe0c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9fe0c-123">Requirement</span></span> | <span data-ttu-id="9fe0c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9fe0c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe0c-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fe0c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe0c-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fe0c-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9fe0c-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fe0c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe0c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fe0c-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9fe0c-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9fe0c-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="9fe0c-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fe0c-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9fe0c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9fe0c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fe0c-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fe0c-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9fe0c-133">IID</span><span class="sxs-lookup"><span data-stu-id="9fe0c-133">IID</span></span><br/>                      | <span data-ttu-id="9fe0c-134">IID \_ имстскнонскриптабле определен как c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="9fe0c-134">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fe0c-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fe0c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe0c-136">**имстскнонскриптабле**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-136">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





