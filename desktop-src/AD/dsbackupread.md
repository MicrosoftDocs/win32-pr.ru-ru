---
title: Функция Дсбаккупреад (Нтдсбкли. h)
description: Считывает блок данных из текущего открытого файла в буфер.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккупреад
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409c2a7d93503aad4edff88070c0458efc961d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988560"
---
# <a name="dsbackupread-function"></a><span data-ttu-id="4c83b-104">Функция Дсбаккупреад</span><span class="sxs-lookup"><span data-stu-id="4c83b-104">DsBackupRead function</span></span>

<span data-ttu-id="4c83b-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4c83b-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4c83b-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="4c83b-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="4c83b-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="4c83b-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="4c83b-108">Функция **дсбаккупреад** считывает блок данных из текущего открытого файла в буфер.</span><span class="sxs-lookup"><span data-stu-id="4c83b-108">The **DsBackupRead** function reads a block of data from the current open file, into a buffer.</span></span> <span data-ttu-id="4c83b-109">Клиентское приложение должно вызывать эту функцию несколько раз, пока не будет получен весь файл резервной копии.</span><span class="sxs-lookup"><span data-stu-id="4c83b-109">The client application is expected to call this function repeatedly until the entire backup file has been received.</span></span> <span data-ttu-id="4c83b-110">Функция [**дсбаккупопенфиле**](dsbackupopenfile.md) предоставляет весь размер файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="4c83b-110">The [**DsBackupOpenFile**](dsbackupopenfile.md) function provides the entire size of the backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c83b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c83b-111">Syntax</span></span>


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="4c83b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c83b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c83b-113">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c83b-113">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c83b-114">Содержит описатель контекста резервного копирования, полученный с помощью функции [**дсбаккуппрепаре**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="4c83b-114">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4c83b-115">*пвбуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c83b-115">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c83b-116">Указатель на буфер, который получает данные.</span><span class="sxs-lookup"><span data-stu-id="4c83b-116">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="4c83b-117">Размер этого буфера должен быть не менее *кббуффер* байт.</span><span class="sxs-lookup"><span data-stu-id="4c83b-117">This buffer must be at least *cbBuffer* bytes in size.</span></span>

</dd> <dt>

<span data-ttu-id="4c83b-118">*кббуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c83b-118">*cbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c83b-119">Содержит размер буфера (в байтах) в *пвбуффер*.</span><span class="sxs-lookup"><span data-stu-id="4c83b-119">Contains the size, in bytes, of the buffer at *pvBuffer*.</span></span> <span data-ttu-id="4c83b-120">Это значение должно быть кратным 8192 и должно быть больше или равно 24576.</span><span class="sxs-lookup"><span data-stu-id="4c83b-120">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="4c83b-121">*пкбреад* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4c83b-121">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c83b-122">Указатель на значение **DWORD** , которое получает фактическое число считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="4c83b-122">Pointer to a **DWORD** value that receives the actual number of bytes read.</span></span> <span data-ttu-id="4c83b-123">Это число может быть меньше запрошенного количества байтов, так как некоторые транспортные фрагменты передаются в буфере вместо того, чтобы заполнять весь буфер данными.</span><span class="sxs-lookup"><span data-stu-id="4c83b-123">This may be less than the number of bytes requested because some transports fragment the buffer being transmitted instead of filling the entire buffer with data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c83b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c83b-124">Return value</span></span>

<span data-ttu-id="4c83b-125">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4c83b-125">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="4c83b-126">Ниже перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="4c83b-126">Possible error codes include the following.</span></span>

<dl> <dt>

<span data-ttu-id="4c83b-127">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="4c83b-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="4c83b-128">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="4c83b-128">One or more parameters are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4c83b-129">**Ошибка при \_ обработке \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="4c83b-129">**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd>

<span data-ttu-id="4c83b-130">Достигнут конец файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="4c83b-130">The end of the backup file was reached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c83b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4c83b-131">Requirements</span></span>



| <span data-ttu-id="4c83b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4c83b-132">Requirement</span></span> | <span data-ttu-id="4c83b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4c83b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c83b-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c83b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4c83b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c83b-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c83b-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c83b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4c83b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c83b-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c83b-138">Header</span><span class="sxs-lookup"><span data-stu-id="4c83b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c83b-139"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c83b-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c83b-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4c83b-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c83b-141"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c83b-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="4c83b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4c83b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c83b-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c83b-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c83b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c83b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c83b-145">**дсбаккупопенфиле**</span><span class="sxs-lookup"><span data-stu-id="4c83b-145">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="4c83b-146">**дсбаккуппрепаре**</span><span class="sxs-lookup"><span data-stu-id="4c83b-146">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="4c83b-147">**дсбаккупфри**</span><span class="sxs-lookup"><span data-stu-id="4c83b-147">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="4c83b-148">Резервное копирование сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="4c83b-148">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="4c83b-149">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="4c83b-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

