---
description: Предоставляет указанное состояние доверия общего ресурса DDE в контексте текущего пользователя.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: Функция Нддесеттрустедшаре (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539962"
---
# <a name="nddesettrustedshare-function"></a><span data-ttu-id="5dd64-103">Функция Нддесеттрустедшаре</span><span class="sxs-lookup"><span data-stu-id="5dd64-103">NDdeSetTrustedShare function</span></span>

<span data-ttu-id="5dd64-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5dd64-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="5dd64-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="5dd64-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="5dd64-106">Предоставляет указанное состояние доверия общего ресурса DDE в контексте текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="5dd64-106">Grants the specified DDE share trusted status within the current user's context.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd64-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dd64-107">Syntax</span></span>


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a><span data-ttu-id="5dd64-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dd64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd64-109">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5dd64-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd64-110">Имя сервера, DSDM которого необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="5dd64-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="5dd64-111">*лпсзшаренаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5dd64-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd64-112">Имя общего ресурса, которому будет предоставлено состояние доверия.</span><span class="sxs-lookup"><span data-stu-id="5dd64-112">The name of the share to be granted trusted status.</span></span> <span data-ttu-id="5dd64-113">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5dd64-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5dd64-114">*двтрустоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5dd64-114">*dwTrustOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd64-115">Параметры, влияющие на состояние доверия общего ресурса DDE.</span><span class="sxs-lookup"><span data-stu-id="5dd64-115">The options affecting the trusted status of the DDE share.</span></span> <span data-ttu-id="5dd64-116">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="5dd64-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="5dd64-117">Параметр</span><span class="sxs-lookup"><span data-stu-id="5dd64-117">Option</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="5dd64-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5dd64-118">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="5dd64-119"><dt>**Ндде \_ Команда " \_ Показывать \_ маску**</dt> <dt>0x0000FFFFL</dt> "</span><span class="sxs-lookup"><span data-stu-id="5dd64-119"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="5dd64-120">Маска, используемая для получения значения, используемого для переопределения общего ресурса DDE, если \_ \_ задано ндде Trust cmd \_ Set.</span><span class="sxs-lookup"><span data-stu-id="5dd64-120">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="5dd64-121"><dt>**Ндде \_ ДОВЕРЯТЬ \_ cmd \_ Показывать**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="5dd64-121"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="5dd64-122">Переопределите состояние показа, указанное в общей папке DDE DSDM.</span><span class="sxs-lookup"><span data-stu-id="5dd64-122">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="5dd64-123"><dt>**Ндде \_ ДОВЕРЯТЬ \_ общему ресурсу \_ Del**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="5dd64-123"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="5dd64-124">Удалите доверенное состояние общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="5dd64-124">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="5dd64-125"><dt>**Ндде \_ 0x40000000L \_ для \_ инициализации общего ресурса**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5dd64-125"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="5dd64-126">Разрешить клиенту инициировать запуск приложения, если он уже выполняется в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="5dd64-126">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="5dd64-127"><dt>**Ндде \_ ДОВЕРЕНный \_ общий ресурс \_ Start**</dt> <dt>0x80000000L</dt></span><span class="sxs-lookup"><span data-stu-id="5dd64-127"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="5dd64-128">Разрешить запуск приложения в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="5dd64-128">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dd64-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dd64-129">Return value</span></span>

<span data-ttu-id="5dd64-130">Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="5dd64-130">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="5dd64-131">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="5dd64-131">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5dd64-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5dd64-132">Remarks</span></span>

<span data-ttu-id="5dd64-133">Общий ресурс DDE сначала должен быть создан с помощью [**нддешареадд**](nddeshareadd.md).</span><span class="sxs-lookup"><span data-stu-id="5dd64-133">The DDE share must first be created with [**NDdeShareAdd**](nddeshareadd.md).</span></span>

<span data-ttu-id="5dd64-134">Если **нддесеттрустедшаре** вызывается с параметром *двтрустоптионс* , для которого установлено значение 0, доверенный общий ресурс теряет свое состояние доверия.</span><span class="sxs-lookup"><span data-stu-id="5dd64-134">If **NDdeSetTrustedShare** is called with *dwTrustOptions* set to zero, the trusted share loses its trusted status.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dd64-135">Требования</span><span class="sxs-lookup"><span data-stu-id="5dd64-135">Requirements</span></span>



| <span data-ttu-id="5dd64-136">Требование</span><span class="sxs-lookup"><span data-stu-id="5dd64-136">Requirement</span></span> | <span data-ttu-id="5dd64-137">Значение</span><span class="sxs-lookup"><span data-stu-id="5dd64-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd64-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5dd64-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5dd64-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5dd64-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5dd64-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5dd64-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5dd64-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5dd64-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5dd64-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5dd64-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dd64-143"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dd64-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dd64-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5dd64-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="5dd64-145"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5dd64-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5dd64-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5dd64-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dd64-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dd64-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="5dd64-148">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="5dd64-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5dd64-149">**Нддесеттрустедшарев** (Юникод) и **нддесеттрустедшареа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5dd64-149">**NDdeSetTrustedShareW** (Unicode) and **NDdeSetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="5dd64-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dd64-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd64-151">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="5dd64-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="5dd64-152">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="5dd64-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="5dd64-153">**нддешареадд**</span><span class="sxs-lookup"><span data-stu-id="5dd64-153">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




