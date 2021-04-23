---
title: Функция Дсбаккупопенфиле (Нтдсбкли. h)
description: Открывает указанный файл и выполняет операции клиента и сервера, необходимые для подготовки файла к резервному копированию.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккупопенфиле
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136150"
---
# <a name="dsbackupopenfile-function"></a><span data-ttu-id="4deae-104">Функция Дсбаккупопенфиле</span><span class="sxs-lookup"><span data-stu-id="4deae-104">DsBackupOpenFile function</span></span>

<span data-ttu-id="4deae-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4deae-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4deae-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="4deae-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="4deae-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="4deae-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="4deae-108">Функция **дсбаккупопенфиле** открывает указанный файл и выполняет операции клиента и сервера, необходимые для подготовки файла к резервному копированию.</span><span class="sxs-lookup"><span data-stu-id="4deae-108">The **DsBackupOpenFile** function opens the specified file and performs the client and server operations necessary to prepare the file for backup.</span></span>

## <a name="syntax"></a><span data-ttu-id="4deae-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4deae-109">Syntax</span></span>


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a><span data-ttu-id="4deae-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4deae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4deae-111">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4deae-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4deae-112">Содержит описатель контекста резервного копирования, полученный с помощью функции [**дсбаккуппрепаре**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="4deae-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4deae-113">*сзаттачментнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4deae-113">*szAttachmentName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4deae-114">Указатель на строку, завершающуюся нулем, которая указывает имя открываемого файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="4deae-114">Pointer to a null-terminated string that specifies the name of the backup file to open.</span></span>

</dd> <dt>

<span data-ttu-id="4deae-115">*кбреадхинтсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4deae-115">*cbReadHintSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4deae-116">Содержит возможный размер (в байтах) буфера, переданного в качестве аргумента *пвбуффер* в функции [**дсбаккупреад**](dsbackupread.md) .</span><span class="sxs-lookup"><span data-stu-id="4deae-116">Contains the possible size, in bytes, of the buffer passed as the *pvBuffer* argument in the [**DsBackupRead**](dsbackupread.md) function.</span></span> <span data-ttu-id="4deae-117">Функции резервного копирования используют это значение в качестве подсказки для оптимизации сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="4deae-117">The backup functions use this value as a hint to optimize the network traffic.</span></span> <span data-ttu-id="4deae-118">Это значение должно быть кратным 8192 и должно быть больше или равно 24576.</span><span class="sxs-lookup"><span data-stu-id="4deae-118">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="4deae-119">*плифилесизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4deae-119">*pliFileSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4deae-120">Указатель на **большое \_ целочисленное** значение, которое получает размер файла резервной копии (в байтах).</span><span class="sxs-lookup"><span data-stu-id="4deae-120">Pointer to a **LARGE\_INTEGER** value that receives the size, in bytes, of the backup file opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4deae-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4deae-121">Return value</span></span>

<span data-ttu-id="4deae-122">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4deae-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="4deae-123">В следующем списке перечислены другие возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="4deae-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="4deae-124">**Ошибка \_ отказа в доступе \_**</span><span class="sxs-lookup"><span data-stu-id="4deae-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="4deae-125">Вызывающий объект не имеет необходимых прав доступа для вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="4deae-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="4deae-126">Функцию [**дссетаусидентити**](dssetauthidentity.md) можно использовать для задания учетных данных, используемых для функций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="4deae-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="4deae-127">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="4deae-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="4deae-128">недопустимые *ХБК*, *сзаттачментнаме* или *плифилесизе* .</span><span class="sxs-lookup"><span data-stu-id="4deae-128">*hbc*, *szAttachmentName*, or *pliFileSize* are invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4deae-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4deae-129">Requirements</span></span>



| <span data-ttu-id="4deae-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4deae-130">Requirement</span></span> | <span data-ttu-id="4deae-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4deae-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4deae-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4deae-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4deae-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4deae-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4deae-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4deae-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4deae-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4deae-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4deae-136">Header</span><span class="sxs-lookup"><span data-stu-id="4deae-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4deae-137"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="4deae-137"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="4deae-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4deae-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="4deae-139"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4deae-139"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="4deae-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4deae-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4deae-141"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4deae-141"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="4deae-142">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4deae-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4deae-143">**Дсбаккупопенфилев** (Юникод) и **дсбаккупопенфилеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4deae-143">**DsBackupOpenFileW** (Unicode) and **DsBackupOpenFileA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="4deae-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4deae-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4deae-145">**дсбаккупреад**</span><span class="sxs-lookup"><span data-stu-id="4deae-145">**DsBackupRead**</span></span>](dsbackupread.md)
</dt> <dt>

[<span data-ttu-id="4deae-146">Резервное копирование сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="4deae-146">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="4deae-147">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="4deae-147">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

