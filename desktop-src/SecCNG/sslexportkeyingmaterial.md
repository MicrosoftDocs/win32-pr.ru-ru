---
description: Экспорт материала ключа на стандарт RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Функция Сслекспорткэйингматериал (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818497"
---
# <a name="sslexportkeyingmaterial-function"></a><span data-ttu-id="b95e2-103">Функция Сслекспорткэйингматериал</span><span class="sxs-lookup"><span data-stu-id="b95e2-103">SslExportKeyingMaterial function</span></span>

<span data-ttu-id="b95e2-104">Экспорт материала ключа на [Стандарт RFC 5705](https://tools.ietf.org/html/rfc5705).</span><span class="sxs-lookup"><span data-stu-id="b95e2-104">Exports keying material per the [RFC 5705 standard](https://tools.ietf.org/html/rfc5705).</span></span> <span data-ttu-id="b95e2-105">Эта функция использует TLS-функцию псевдослучайное для создания байтового буфера материала для создания ключа.</span><span class="sxs-lookup"><span data-stu-id="b95e2-105">This function uses the TLS pseudorandom function to produce a byte buffer of keying material.</span></span> <span data-ttu-id="b95e2-106">Он принимает ссылку на главный секрет, метку ASCII дисамбигуатинг, случайные значения Client и Server, а также, при необходимости, данные контекста приложения.</span><span class="sxs-lookup"><span data-stu-id="b95e2-106">It takes a reference to the master secret, the disambiguating ASCII label, client and server random values, and optionally the application context data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b95e2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b95e2-107">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b95e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b95e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b95e2-109">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-109">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b95e2-110">Маркер экземпляра поставщика протокола TLS.</span><span class="sxs-lookup"><span data-stu-id="b95e2-110">The handle of the TLS protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="b95e2-111">*хмастеркэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-111">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b95e2-112">Маркер объекта главного ключа, который будет использоваться для создания материала для ключа, экспортируемого в br.</span><span class="sxs-lookup"><span data-stu-id="b95e2-112">The handle of the master key object that will be used to create the keying material to br exported.</span></span>

</dd> <dt>

<span data-ttu-id="b95e2-113">*слабел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-113">*sLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b95e2-114">строка метки ASCII, заканчивающаяся на NUL.</span><span class="sxs-lookup"><span data-stu-id="b95e2-114">a NUL-terminated ASCII label string.</span></span> <span data-ttu-id="b95e2-115">Schannel Удаляет завершающий символ NUL перед передачей функции псевдослучайное.</span><span class="sxs-lookup"><span data-stu-id="b95e2-115">Schannel will remove the terminating NUL character before passing it to the pseudorandom function.</span></span>

</dd> <dt>

<span data-ttu-id="b95e2-116">*пбрандомс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-116">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b95e2-117">Указатель на буфер, который содержит сцепление *\_ случайных* и *серверных \_ случайных* значений подключения TLS.</span><span class="sxs-lookup"><span data-stu-id="b95e2-117">A pointer to a buffer that contains a concatenation of the *client\_random* and *server\_random* values of the TLS connection.</span></span>

</dd> <dt>

<span data-ttu-id="b95e2-118">*кбрандомс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-118">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b95e2-119">Длина буфера *пбрандомс* в байтах.</span><span class="sxs-lookup"><span data-stu-id="b95e2-119">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b95e2-120">*пбконтекствалуе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-120">*pbContextValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b95e2-121">Указатель на буфер, содержащий контекст приложения.</span><span class="sxs-lookup"><span data-stu-id="b95e2-121">A pointer to a buffer that contains the application context.</span></span> <span data-ttu-id="b95e2-122">Если *пбконтекствалуе* имеет **значение NULL**, *кбконтекствалуе* должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="b95e2-122">If *pbContextValue* is **NULL**, *cbContextValue* must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b95e2-123">*кбконтекствалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-123">*cbContextValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b95e2-124">Длина буфера *пбконтекствалуе* в байтах.</span><span class="sxs-lookup"><span data-stu-id="b95e2-124">The length, in bytes, of the *pbContextValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b95e2-125">*пбаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-125">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b95e2-126">Адрес буфера, который получает экспортированный материал ключа.</span><span class="sxs-lookup"><span data-stu-id="b95e2-126">The address of a buffer that receives the exported keying material.</span></span> <span data-ttu-id="b95e2-127">Параметр *кбаутпут* содержит размер этого буфера.</span><span class="sxs-lookup"><span data-stu-id="b95e2-127">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="b95e2-128">Это значение не может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="b95e2-128">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b95e2-129">*кбаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-129">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b95e2-130">Длина буфера *пбаутпут* в байтах.</span><span class="sxs-lookup"><span data-stu-id="b95e2-130">The length, in bytes, of the *pbOutput* buffer.</span></span> <span data-ttu-id="b95e2-131">Должен быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="b95e2-131">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="b95e2-132">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b95e2-133">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b95e2-133">Not used.</span></span> <span data-ttu-id="b95e2-134">Необходимо задать значение 0.</span><span class="sxs-lookup"><span data-stu-id="b95e2-134">Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b95e2-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b95e2-135">Return value</span></span>

<span data-ttu-id="b95e2-136">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b95e2-136">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="b95e2-137">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="b95e2-137">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="b95e2-138">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="b95e2-138">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="b95e2-139">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b95e2-139">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="b95e2-140">Описание</span><span class="sxs-lookup"><span data-stu-id="b95e2-140">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="b95e2-141">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b95e2-141"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="b95e2-142">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="b95e2-142">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b95e2-143">Требования</span><span class="sxs-lookup"><span data-stu-id="b95e2-143">Requirements</span></span>



| <span data-ttu-id="b95e2-144">Требование</span><span class="sxs-lookup"><span data-stu-id="b95e2-144">Requirement</span></span> | <span data-ttu-id="b95e2-145">Значение</span><span class="sxs-lookup"><span data-stu-id="b95e2-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b95e2-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b95e2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b95e2-147">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-147">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b95e2-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b95e2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b95e2-149">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="b95e2-149">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b95e2-150">Header</span><span class="sxs-lookup"><span data-stu-id="b95e2-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b95e2-151"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="b95e2-151"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="b95e2-152">DLL</span><span class="sxs-lookup"><span data-stu-id="b95e2-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b95e2-153"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b95e2-153"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




