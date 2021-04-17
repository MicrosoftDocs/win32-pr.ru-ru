---
description: Задает дескриптор безопасности, связанный с общим ресурсом DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Функция Нддесетшаресекурити (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683880"
---
# <a name="nddesetsharesecurity-function"></a><span data-ttu-id="2072a-103">Функция Нддесетшаресекурити</span><span class="sxs-lookup"><span data-stu-id="2072a-103">NDdeSetShareSecurity function</span></span>

<span data-ttu-id="2072a-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2072a-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="2072a-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="2072a-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="2072a-106">Задает дескриптор безопасности, связанный с общим ресурсом DDE.</span><span class="sxs-lookup"><span data-stu-id="2072a-106">Sets the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="2072a-107">Это обычно происходит после изменения списка DACL, назначенного общему ресурсу DDE.</span><span class="sxs-lookup"><span data-stu-id="2072a-107">This is done usually after editing the DACL assigned to the DDE share.</span></span>

## <a name="syntax"></a><span data-ttu-id="2072a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2072a-108">Syntax</span></span>


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a><span data-ttu-id="2072a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2072a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2072a-110">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2072a-110">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072a-111">Имя сервера, DSDM которого необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="2072a-111">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="2072a-112">*лпсзшаренаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2072a-112">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072a-113">Имя общей папки, дескриптор безопасности которой необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="2072a-113">The name of the share whose security descriptor is to be modified.</span></span> <span data-ttu-id="2072a-114">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2072a-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2072a-115">*Si* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2072a-115">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072a-116">Значение [**\_ сведений о безопасности**](/windows/desktop/SecAuthZ/security-information) , идентифицирующее сведения о безопасности для извлечения.</span><span class="sxs-lookup"><span data-stu-id="2072a-116">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that identifies the security information to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="2072a-117">*pSD* \[ - окне\]</span><span class="sxs-lookup"><span data-stu-id="2072a-117">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2072a-118">Указатель на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , содержащую сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="2072a-118">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains security information.</span></span> <span data-ttu-id="2072a-119">Этот параметр не может иметь **значение NULL** и указывать на допустимый дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="2072a-119">This parameter cannot be **NULL** and should point to a valid security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2072a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2072a-120">Return value</span></span>

<span data-ttu-id="2072a-121">Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="2072a-121">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="2072a-122">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="2072a-122">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2072a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2072a-123">Remarks</span></span>

<span data-ttu-id="2072a-124">Чтобы изменить [**\_ дескриптор безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , связанный с общим ресурсом DDE в DSDM, пользователь должен иметь соответствующие права доступа. Автор общей папки имеет эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="2072a-124">To modify the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associated with a DDE share in the DSDM, the user must have appropriate privilege; the share creator has this privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="2072a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2072a-125">Requirements</span></span>



| <span data-ttu-id="2072a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2072a-126">Requirement</span></span> | <span data-ttu-id="2072a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2072a-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2072a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2072a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2072a-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2072a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2072a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2072a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2072a-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2072a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2072a-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2072a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2072a-133"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2072a-133"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="2072a-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2072a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="2072a-135"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2072a-135"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2072a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2072a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2072a-137"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2072a-137"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="2072a-138">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="2072a-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2072a-139">**Нддесетшаресекуритив** (Юникод) и **нддесетшаресекуритя** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2072a-139">**NDdeSetShareSecurityW** (Unicode) and **NDdeSetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="2072a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2072a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2072a-141">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="2072a-141">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="2072a-142">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="2072a-142">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="2072a-143">**\_сведения о безопасности**</span><span class="sxs-lookup"><span data-stu-id="2072a-143">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="2072a-144">**нддежетшаресекурити**</span><span class="sxs-lookup"><span data-stu-id="2072a-144">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)
</dt> </dl>

 

