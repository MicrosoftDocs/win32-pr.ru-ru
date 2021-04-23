---
description: Извлекает дескриптор безопасности, связанный с общим ресурсом DDE. Обычно это делается для редактирования.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Функция Нддежетшаресекурити (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912971"
---
# <a name="nddegetsharesecurity-function"></a><span data-ttu-id="b8e3a-104">Функция Нддежетшаресекурити</span><span class="sxs-lookup"><span data-stu-id="b8e3a-104">NDdeGetShareSecurity function</span></span>

<span data-ttu-id="b8e3a-105">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="b8e3a-106">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="b8e3a-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="b8e3a-107">Извлекает дескриптор безопасности, связанный с общим ресурсом DDE.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-107">Retrieves the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="b8e3a-108">Обычно это делается для редактирования.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-108">This is done usually for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e3a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8e3a-109">Syntax</span></span>


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
);
```



## <a name="parameters"></a><span data-ttu-id="b8e3a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8e3a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e3a-111">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8e3a-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e3a-112">Имя сервера, на котором находится DSDM.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="b8e3a-113">*лпсзшаренаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8e3a-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e3a-114">Имя общей папки, дескриптор безопасности которой необходимо получить из DSDM.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-114">The name of the share whose security descriptor is to be retrieved from the DSDM.</span></span> <span data-ttu-id="b8e3a-115">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8e3a-116">*Si* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8e3a-116">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e3a-117">Значение [**\_ сведений о безопасности**](/windows/desktop/SecAuthZ/security-information) , указывающее сведения о безопасности, которые необходимо получить из дескриптора безопасности, связанного с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-117">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that specifies the security information to be retrieved from the security descriptor associated with the share.</span></span>

</dd> <dt>

<span data-ttu-id="b8e3a-118">*pSD* \[ - заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b8e3a-118">*pSD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e3a-119">Указатель на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , которая получает собственный дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-119">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that receives the self-relative security descriptor.</span></span> <span data-ttu-id="b8e3a-120">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-120">This parameter can be **NULL**.</span></span> <span data-ttu-id="b8e3a-121">Если этот параметр имеет **значение NULL**, DSDM определяет размер запрашиваемых сведений о безопасности и возвращает число байтов, необходимое в параметре *лпкбсдрекуиред* , а также ндде \_ buf \_ слишком \_ маленький код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-121">If this parameter is **NULL**, the DSDM determines the size of the requested security information and returns the number of bytes needed in the *lpcbsdRequired* parameter along with the NDDE\_BUF\_TOO\_SMALL error code.</span></span>

</dd> <dt>

<span data-ttu-id="b8e3a-122">*кбсд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8e3a-122">*cbSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e3a-123">Размер буфера *pSD* .</span><span class="sxs-lookup"><span data-stu-id="b8e3a-123">The size of the *pSD* buffer.</span></span> <span data-ttu-id="b8e3a-124">Если *pSD* имеет **значение NULL**, этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-124">This parameter must be zero if *pSD* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8e3a-125">*лпкбсдрекуиред* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b8e3a-125">*lpcbsdRequired* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e3a-126">Указатель на переменную, которая получает фактический размер полученного дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-126">A pointer to the variable that receives the actual size of the retrieved security descriptor.</span></span> <span data-ttu-id="b8e3a-127">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e3a-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8e3a-128">Return value</span></span>

<span data-ttu-id="b8e3a-129">Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="b8e3a-130">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="b8e3a-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="b8e3a-131">Если параметр *pSD* имел **значение NULL**, он возвращает ндде \_ buf \_ слишком \_ мал.</span><span class="sxs-lookup"><span data-stu-id="b8e3a-131">If the *pSD* parameter was **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e3a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b8e3a-132">Requirements</span></span>



| <span data-ttu-id="b8e3a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b8e3a-133">Requirement</span></span> | <span data-ttu-id="b8e3a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b8e3a-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e3a-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8e3a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b8e3a-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8e3a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b8e3a-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8e3a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b8e3a-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8e3a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b8e3a-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b8e3a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8e3a-140"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8e3a-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8e3a-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b8e3a-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8e3a-142"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8e3a-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8e3a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b8e3a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8e3a-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8e3a-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="b8e3a-145">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="b8e3a-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b8e3a-146">**Нддежетшаресекуритив** (Юникод) и **нддежетшаресекуритя** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b8e3a-146">**NDdeGetShareSecurityW** (Unicode) and **NDdeGetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="b8e3a-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8e3a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e3a-148">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="b8e3a-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="b8e3a-149">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="b8e3a-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="b8e3a-150">**\_сведения о безопасности**</span><span class="sxs-lookup"><span data-stu-id="b8e3a-150">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="b8e3a-151">**нддесетшаресекурити**</span><span class="sxs-lookup"><span data-stu-id="b8e3a-151">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> </dl>

 

