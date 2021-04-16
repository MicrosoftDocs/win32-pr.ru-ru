---
title: Функция Дссетаусидентити (Нтдсбкли. h)
description: Задает контекст безопасности, в котором вызываются API-интерфейсы резервного копирования каталога.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дссетаусидентити
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491235"
---
# <a name="dssetauthidentity-function"></a><span data-ttu-id="cbc3a-104">Функция Дссетаусидентити</span><span class="sxs-lookup"><span data-stu-id="cbc3a-104">DsSetAuthIdentity function</span></span>

<span data-ttu-id="cbc3a-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="cbc3a-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cbc3a-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="cbc3a-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="cbc3a-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="cbc3a-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="cbc3a-108">Функция **дссетаусидентити** задает контекст безопасности, в котором вызываются API-интерфейсы резервного копирования каталога.</span><span class="sxs-lookup"><span data-stu-id="cbc3a-108">The **DsSetAuthIdentity** function sets the security context under which the directory backup APIs are called.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc3a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbc3a-109">Syntax</span></span>


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a><span data-ttu-id="cbc3a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbc3a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc3a-111">*сзусернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbc3a-111">*szUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc3a-112">Строка, завершающаяся нулем, которая указывает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="cbc3a-112">The null-terminated string that specifies the user name.</span></span>

</dd> <dt>

<span data-ttu-id="cbc3a-113">*сздомаиннаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbc3a-113">*szDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc3a-114">Строка, завершающаяся нулем, которая указывает имя домена, к которому принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="cbc3a-114">The null-terminated string that specifies the name of the domain that the user belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="cbc3a-115">*сзпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbc3a-115">*szPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc3a-116">Строка, завершающаяся нулем, которая указывает пароль пользователя в указанном домене.</span><span class="sxs-lookup"><span data-stu-id="cbc3a-116">The null-terminated string that specifies the password of the user in the specified domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc3a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbc3a-117">Return value</span></span>

<span data-ttu-id="cbc3a-118">В случае успеха возвращает стандартные коды успешного выполнения **HRESULT** . в противном случае возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="cbc3a-118">If successful, returns a standard **HRESULT** success codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc3a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbc3a-119">Remarks</span></span>

<span data-ttu-id="cbc3a-120">Если **дссетаусидентити** не вызывается, предполагается, что используется контекст безопасности текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="cbc3a-120">If **DsSetAuthIdentity** is not called, security context of the current process is assumed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc3a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cbc3a-121">Requirements</span></span>



| <span data-ttu-id="cbc3a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cbc3a-122">Requirement</span></span> | <span data-ttu-id="cbc3a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cbc3a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc3a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbc3a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc3a-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbc3a-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbc3a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbc3a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc3a-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbc3a-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbc3a-128">Header</span><span class="sxs-lookup"><span data-stu-id="cbc3a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbc3a-129"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbc3a-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="cbc3a-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cbc3a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="cbc3a-131"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbc3a-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="cbc3a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cbc3a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbc3a-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbc3a-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="cbc3a-134">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="cbc3a-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cbc3a-135">**Дссетаусидентитив** (Юникод) и **дссетаусидентитя** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cbc3a-135">**DsSetAuthIdentityW** (Unicode) and **DsSetAuthIdentityA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="cbc3a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbc3a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc3a-137">Резервное копирование и восстановление сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="cbc3a-137">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="cbc3a-138">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="cbc3a-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

