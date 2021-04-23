---
description: Возвращает размер сертификата для драйвера экрана.
ms.assetid: fd52e939-127a-4493-8406-31f7767921cd
title: Функция Жетцертификатесизе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateSize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bcd1f49ce65978c6a89c89cee1fda38e41434065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342455"
---
# <a name="getcertificatesize-function"></a><span data-ttu-id="e44d0-103">Функция Жетцертификатесизе</span><span class="sxs-lookup"><span data-stu-id="e44d0-103">GetCertificateSize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e44d0-104">Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="e44d0-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="e44d0-105">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="e44d0-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="e44d0-106">Возвращает размер сертификата для драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="e44d0-106">Gets the size of a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44d0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e44d0-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificateSize(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ ULONG                    *pulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="e44d0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e44d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e44d0-109">*пстрдевиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44d0-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44d0-110">Указатель на [**\_ строковую структуру Юникода**](/windows/win32/api/subauth/ns-subauth-unicode_string) , содержащую имя устройства вывода, которое возвращается функцией [**жетмониторинфо**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="e44d0-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="e44d0-111">*ктпвпцертификатетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44d0-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44d0-112">Тип сертификата, указанный как член перечисления **\_ \_ типа сертификата дксгкмдт** .</span><span class="sxs-lookup"><span data-stu-id="e44d0-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e44d0-113">*пулцертификателенгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e44d0-113">*pulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e44d0-114">Получает размер сертификата в байтах.</span><span class="sxs-lookup"><span data-stu-id="e44d0-114">Receives the size of the certificate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e44d0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e44d0-115">Return value</span></span>

<span data-ttu-id="e44d0-116">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="e44d0-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="e44d0-117">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="e44d0-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e44d0-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e44d0-118">Remarks</span></span>

<span data-ttu-id="e44d0-119">Приложения должны вызывать метод [**иопмвидеуутпут:: стартинитиализатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) вместо этой функции.</span><span class="sxs-lookup"><span data-stu-id="e44d0-119">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="e44d0-120">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="e44d0-120">This function has no associated import library.</span></span> <span data-ttu-id="e44d0-121">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="e44d0-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e44d0-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e44d0-122">Requirements</span></span>



| <span data-ttu-id="e44d0-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e44d0-123">Requirement</span></span> | <span data-ttu-id="e44d0-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e44d0-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e44d0-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e44d0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e44d0-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e44d0-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e44d0-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e44d0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e44d0-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e44d0-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e44d0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e44d0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e44d0-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e44d0-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e44d0-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e44d0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e44d0-132">Функции ОПМ</span><span class="sxs-lookup"><span data-stu-id="e44d0-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="e44d0-133">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="e44d0-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
