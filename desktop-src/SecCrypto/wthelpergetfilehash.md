---
description: Проверяет подпись подписанного файла и получает хэш-значение и идентификатор алгоритма для файла.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: Функция Вселпержетфилехаш
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998623"
---
# <a name="wthelpergetfilehash-function"></a><span data-ttu-id="603ec-103">Функция Вселпержетфилехаш</span><span class="sxs-lookup"><span data-stu-id="603ec-103">WTHelperGetFileHash function</span></span>

<span data-ttu-id="603ec-104">\[Функция **вселпержетфилехаш** доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="603ec-104">\[The **WTHelperGetFileHash** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="603ec-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="603ec-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="603ec-106">Функция **вселпержетфилехаш** проверяет подпись подписанного файла и получает хэш-значение и идентификатор алгоритма для файла.</span><span class="sxs-lookup"><span data-stu-id="603ec-106">The **WTHelperGetFileHash** function verifies the signature of a signed file and obtains the hash value and algorithm identifier for the file.</span></span>

> [!Note]  
> <span data-ttu-id="603ec-107">Эта функция не объявлена в опубликованном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="603ec-107">This function is not declared in a published header file.</span></span> <span data-ttu-id="603ec-108">Чтобы использовать эту функцию, объявите ее в точно указанном формате.</span><span class="sxs-lookup"><span data-stu-id="603ec-108">To use this function, declare it in the exact format shown.</span></span> <span data-ttu-id="603ec-109">Эта функция также не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="603ec-109">This function also has no associated import library.</span></span> <span data-ttu-id="603ec-110">Для динамической привязки к Wintrust.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="603ec-110">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="603ec-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="603ec-111">Syntax</span></span>


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a><span data-ttu-id="603ec-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="603ec-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="603ec-113">*пвсзфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="603ec-113">*pwszFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="603ec-114">Указатель на строку в Юникоде, заканчивающуюся нулем и содержащую путь и имя файла, для которого нужно получить хэш.</span><span class="sxs-lookup"><span data-stu-id="603ec-114">A pointer to a null-terminated Unicode string that contains the path and file name of the file to get the hash for.</span></span>

</dd> <dt>

<span data-ttu-id="603ec-115">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="603ec-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="603ec-116">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="603ec-116">This parameter is not used and should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="603ec-117">*пвресервед* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="603ec-117">*pvReserved* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="603ec-118">Этот параметр не используется и должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="603ec-118">This parameter is not used and should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="603ec-119">*пбфилехаш* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="603ec-119">*pbFileHash* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="603ec-120">Указатель на буфер для получения хэш-значения для файла.</span><span class="sxs-lookup"><span data-stu-id="603ec-120">A pointer to a buffer to receive the hash value for the file.</span></span> <span data-ttu-id="603ec-121">Параметр *пкбфилехаш* содержит размер этого буфера.</span><span class="sxs-lookup"><span data-stu-id="603ec-121">The *pcbFileHash* parameter contains the size of this buffer.</span></span>

</dd> <dt>

<span data-ttu-id="603ec-122">*пкбфилехаш* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="603ec-122">*pcbFileHash* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="603ec-123">Указатель на переменную **типа DWORD** , которая во входных данных содержит размер (в байтах) буфера *пбфилехаш* , а выходные данные — размер (в байтах) хэш-значения.</span><span class="sxs-lookup"><span data-stu-id="603ec-123">A pointer to a **DWORD** variable that, on input, contains the size, in bytes, of the *pbFileHash* buffer and, on output, receives the size, in bytes, of the hash value.</span></span>

<span data-ttu-id="603ec-124">Чтобы получить необходимый размер хэш-значения, передайте **значение NULL** для параметра *пбфилехаш* .</span><span class="sxs-lookup"><span data-stu-id="603ec-124">To obtain the required size of the hash value, pass **NULL** for the *pbFileHash* parameter.</span></span> <span data-ttu-id="603ec-125">Эта функция поместит требуемый размер (в байтах) хэш-значения в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="603ec-125">This function will place the required size, in bytes, of the hash value in this location.</span></span>

<span data-ttu-id="603ec-126">Если параметр *пбфилехаш* имеет значение, отличное от **null**, и размер не достаточен для получения хэш-значения, эта функция поместит требуемый размер (в байтах) в этом расположении и возвратит **\_ Дополнительные \_ данные об ошибке**.</span><span class="sxs-lookup"><span data-stu-id="603ec-126">If the *pbFileHash* parameter is not **NULL**, and the size is not large enough to receive the hash value, this function will place the required size, in bytes, in this location and return **ERROR\_MORE\_DATA**.</span></span>

</dd> <dt>

<span data-ttu-id="603ec-127">*фашалгид* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="603ec-127">*pHashAlgid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="603ec-128">Указатель на переменную [**\_ идентификатора ALG**](alg-id.md) для получения идентификатора алгоритма, используемого для создания хэш-значения.</span><span class="sxs-lookup"><span data-stu-id="603ec-128">A pointer to an [**ALG\_ID**](alg-id.md) variable to receive the identifier of the algorithm used to create the hash value.</span></span> <span data-ttu-id="603ec-129">Этот параметр может иметь **значение NULL** , если эти сведения не требуются.</span><span class="sxs-lookup"><span data-stu-id="603ec-129">This parameter can be **NULL** if this information is not needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="603ec-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="603ec-130">Return value</span></span>

<span data-ttu-id="603ec-131">Возвращает код состояния, который указывает на успешное или неуспешное завершение функции.</span><span class="sxs-lookup"><span data-stu-id="603ec-131">Returns a status code that indicates the success or failure of the function.</span></span>

<span data-ttu-id="603ec-132">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="603ec-132">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="603ec-133">Код возврата</span><span class="sxs-lookup"><span data-stu-id="603ec-133">Return code</span></span>                                                                                               | <span data-ttu-id="603ec-134">Описание</span><span class="sxs-lookup"><span data-stu-id="603ec-134">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="603ec-135"><dt>**Ошибка при \_ успешном выполнении**</dt></span><span class="sxs-lookup"><span data-stu-id="603ec-135"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>             | <span data-ttu-id="603ec-136">Файл подписан, и подпись проверена.</span><span class="sxs-lookup"><span data-stu-id="603ec-136">The file is signed, and the signature was verified.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="603ec-137"><dt>**Ошибка \_ дополнительных \_ данных**</dt></span><span class="sxs-lookup"><span data-stu-id="603ec-137"><dt>**ERROR\_MORE\_DATA**</dt></span></span> </dl>          | <span data-ttu-id="603ec-138">Параметр *пбфилехаш* не равен **null**, а размер, указанный в параметре *пкбфилехаш* , недостаточно велик для получения хэша.</span><span class="sxs-lookup"><span data-stu-id="603ec-138">The *pbFileHash* parameter is not **NULL**, and the size specified by the *pcbFileHash* parameter is not large enough to receive the hash.</span></span><br/> |
| <dl> <span data-ttu-id="603ec-139"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="603ec-139"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="603ec-140">Ошибка при выделении памяти.</span><span class="sxs-lookup"><span data-stu-id="603ec-140">A memory allocation failure occurred.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="603ec-141"><dt>**ДОВЕРЯТЬ \_ E с \_ неверным \_ дайджестом**</dt></span><span class="sxs-lookup"><span data-stu-id="603ec-141"><dt>**TRUST\_E\_BAD\_DIGEST**</dt></span></span> </dl>      | <span data-ttu-id="603ec-142">Подпись файла не проверена.</span><span class="sxs-lookup"><span data-stu-id="603ec-142">The signature of the file was not verified.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="603ec-143"><dt>**ДОВЕРЯТЬ \_ электронной \_ подписи**</dt></span><span class="sxs-lookup"><span data-stu-id="603ec-143"><dt>**TRUST\_E\_NOSIGNATURE**</dt></span></span> </dl>      | <span data-ttu-id="603ec-144">Файл не подписан или имеет недопустимую подпись.</span><span class="sxs-lookup"><span data-stu-id="603ec-144">The file was not signed or had a signature that is not valid.</span></span><br/>                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="603ec-145">Требования</span><span class="sxs-lookup"><span data-stu-id="603ec-145">Requirements</span></span>



| <span data-ttu-id="603ec-146">Требование</span><span class="sxs-lookup"><span data-stu-id="603ec-146">Requirement</span></span> | <span data-ttu-id="603ec-147">Значение</span><span class="sxs-lookup"><span data-stu-id="603ec-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="603ec-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="603ec-148">Minimum supported client</span></span><br/> | <span data-ttu-id="603ec-149">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="603ec-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="603ec-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="603ec-150">Minimum supported server</span></span><br/> | <span data-ttu-id="603ec-151">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="603ec-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="603ec-152">DLL</span><span class="sxs-lookup"><span data-stu-id="603ec-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="603ec-153"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="603ec-153"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
