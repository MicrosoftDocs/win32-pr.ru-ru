---
title: Функция Дсресторинд (Нтдсбкли. h)
description: Вызывается для завершения операции восстановления.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсресторинд
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabbe216875c2fe934f3c87e32688cd17bc8992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071531"
---
# <a name="dsrestoreend-function"></a><span data-ttu-id="6843e-104">Функция Дсресторинд</span><span class="sxs-lookup"><span data-stu-id="6843e-104">DsRestoreEnd function</span></span>

<span data-ttu-id="6843e-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6843e-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6843e-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="6843e-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6843e-107">Вместо этого используйте [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="6843e-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="6843e-108">Для завершения операции восстановления вызывается функция **дсресторинд** .</span><span class="sxs-lookup"><span data-stu-id="6843e-108">The **DsRestoreEnd** function is called to terminate a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6843e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6843e-109">Syntax</span></span>


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="6843e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6843e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6843e-111">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6843e-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6843e-112">Содержит описатель контекста восстановления, полученный с помощью функции [**дсресторепрепаре**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="6843e-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6843e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6843e-113">Return value</span></span>

<span data-ttu-id="6843e-114">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6843e-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="6843e-115">В следующем списке перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="6843e-115">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="6843e-116">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="6843e-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="6843e-117">Недопустимый *ХБК* .</span><span class="sxs-lookup"><span data-stu-id="6843e-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6843e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6843e-118">Remarks</span></span>

<span data-ttu-id="6843e-119">Функция **дсресторинд** закрывает необработанные дескрипторы привязки и выполняет операцию очистки после попытки восстановления.</span><span class="sxs-lookup"><span data-stu-id="6843e-119">The **DsRestoreEnd** function closes outstanding binding handles and performs a cleanup operation after a restore attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="6843e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6843e-120">Requirements</span></span>



| <span data-ttu-id="6843e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6843e-121">Requirement</span></span> | <span data-ttu-id="6843e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6843e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6843e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6843e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6843e-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6843e-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6843e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6843e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6843e-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6843e-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6843e-127">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6843e-127">End of client support</span></span><br/>    | <span data-ttu-id="6843e-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6843e-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6843e-129">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="6843e-129">End of server support</span></span><br/>    | <span data-ttu-id="6843e-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6843e-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6843e-131">Header</span><span class="sxs-lookup"><span data-stu-id="6843e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6843e-132"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="6843e-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="6843e-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6843e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="6843e-134"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6843e-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="6843e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6843e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6843e-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6843e-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6843e-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6843e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6843e-138">**дсресторепрепаре**</span><span class="sxs-lookup"><span data-stu-id="6843e-138">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="6843e-139">Восстановление сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="6843e-139">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="6843e-140">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="6843e-140">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

