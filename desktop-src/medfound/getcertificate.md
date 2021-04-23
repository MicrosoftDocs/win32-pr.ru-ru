---
description: Возвращает сертификат для драйвера экрана.
ms.assetid: eceaf151-1dae-4ff0-9139-7f1789f6c682
title: Функция Certificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificate
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 30cb17345177b552e51120afd00758a3f6886584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701309"
---
# <a name="getcertificate-function"></a><span data-ttu-id="dfc7b-103">Функция Certificate</span><span class="sxs-lookup"><span data-stu-id="dfc7b-103">GetCertificate function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfc7b-104">Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="dfc7b-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="dfc7b-105">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="dfc7b-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="dfc7b-106">Возвращает сертификат для драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="dfc7b-106">Gets a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc7b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfc7b-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificate(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ BYTE                     *pbCertificate,
  _Out_ ULONG                    ulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="dfc7b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfc7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfc7b-109">*пстрдевиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfc7b-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfc7b-110">Указатель на [**\_ строковую структуру Юникода**](/windows/win32/api/subauth/ns-subauth-unicode_string) , содержащую имя устройства вывода, которое возвращается функцией [**жетмониторинфо**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="dfc7b-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="dfc7b-111">*ктпвпцертификатетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfc7b-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfc7b-112">Тип сертификата, указанный как член перечисления **\_ \_ типа сертификата дксгкмдт** .</span><span class="sxs-lookup"><span data-stu-id="dfc7b-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="dfc7b-113">*пбцертификате* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfc7b-113">*pbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfc7b-114">Указатель на буфер, который получает сертификат.</span><span class="sxs-lookup"><span data-stu-id="dfc7b-114">A pointer to a buffer that receives the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="dfc7b-115">*улцертификателенгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfc7b-115">*ulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfc7b-116">Размер буфера *пбцертификате* в байтах.</span><span class="sxs-lookup"><span data-stu-id="dfc7b-116">The size of the *pbCertificate* buffer, in bytes.</span></span> <span data-ttu-id="dfc7b-117">Чтобы получить размер сертификата, вызовите [**жетцертификатесизе**](getcertificatesize.md).</span><span class="sxs-lookup"><span data-stu-id="dfc7b-117">To get the size of the certificate, call [**GetCertificateSize**](getcertificatesize.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfc7b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfc7b-118">Return value</span></span>

<span data-ttu-id="dfc7b-119">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="dfc7b-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="dfc7b-120">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="dfc7b-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfc7b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfc7b-121">Remarks</span></span>

<span data-ttu-id="dfc7b-122">Приложения должны вызывать метод [**иопмвидеуутпут:: стартинитиализатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) вместо этой функции.</span><span class="sxs-lookup"><span data-stu-id="dfc7b-122">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="dfc7b-123">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="dfc7b-123">This function has no associated import library.</span></span> <span data-ttu-id="dfc7b-124">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="dfc7b-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfc7b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="dfc7b-125">Requirements</span></span>



| <span data-ttu-id="dfc7b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="dfc7b-126">Requirement</span></span> | <span data-ttu-id="dfc7b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="dfc7b-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dfc7b-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfc7b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dfc7b-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfc7b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dfc7b-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfc7b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dfc7b-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dfc7b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dfc7b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dfc7b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfc7b-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfc7b-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfc7b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfc7b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc7b-135">Функции ОПМ</span><span class="sxs-lookup"><span data-stu-id="dfc7b-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="dfc7b-136">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="dfc7b-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
