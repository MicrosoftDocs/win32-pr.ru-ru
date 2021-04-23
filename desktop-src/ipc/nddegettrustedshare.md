---
description: Извлекает параметры, связанные с общим ресурсом DDE, который находится в списке пользователей сервера доверенных общих папок.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Функция Нддежеттрустедшаре (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662151"
---
# <a name="nddegettrustedshare-function"></a><span data-ttu-id="5be42-103">Функция Нддежеттрустедшаре</span><span class="sxs-lookup"><span data-stu-id="5be42-103">NDdeGetTrustedShare function</span></span>

<span data-ttu-id="5be42-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5be42-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="5be42-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="5be42-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="5be42-106">Извлекает параметры, связанные с общим ресурсом DDE, который находится в списке доверенных общих ресурсов пользователя сервера.</span><span class="sxs-lookup"><span data-stu-id="5be42-106">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="5be42-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5be42-107">Syntax</span></span>


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a><span data-ttu-id="5be42-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5be42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5be42-109">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5be42-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be42-110">Имя сервера, на котором находится DSDM.</span><span class="sxs-lookup"><span data-stu-id="5be42-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="5be42-111">*лпсзшаренаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5be42-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be42-112">Имя общего ресурса, состояние доверия которого запрашивается.</span><span class="sxs-lookup"><span data-stu-id="5be42-112">The share name whose trusted status is being queried.</span></span> <span data-ttu-id="5be42-113">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5be42-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5be42-114">*лпдвтрустоптионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5be42-114">*lpdwTrustOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5be42-115">Указатель на переменную, которая получает параметры доверия.</span><span class="sxs-lookup"><span data-stu-id="5be42-115">A pointer to a variable that receives the trust options.</span></span> <span data-ttu-id="5be42-116">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5be42-116">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="5be42-117">Доступны следующие параметры доверия.</span><span class="sxs-lookup"><span data-stu-id="5be42-117">The following trust options are available.</span></span>



| <span data-ttu-id="5be42-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5be42-118">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="5be42-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5be42-119">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="5be42-120"><dt>**Ндде \_ Команда " \_ Показывать \_ маску**</dt> <dt>0x0000FFFFL</dt> "</span><span class="sxs-lookup"><span data-stu-id="5be42-120"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="5be42-121">Маска, используемая для получения значения, используемого для переопределения общего ресурса DDE, если \_ \_ задано ндде Trust cmd \_ Set.</span><span class="sxs-lookup"><span data-stu-id="5be42-121">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="5be42-122"><dt>**Ндде \_ ДОВЕРЯТЬ \_ cmd \_ Показывать**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="5be42-122"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="5be42-123">Переопределите состояние показа, указанное в общей папке DDE DSDM.</span><span class="sxs-lookup"><span data-stu-id="5be42-123">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="5be42-124"><dt>**Ндде \_ ДОВЕРЯТЬ \_ общему ресурсу \_ Del**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="5be42-124"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="5be42-125">Удалите доверенное состояние общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="5be42-125">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="5be42-126"><dt>**Ндде \_ 0x40000000L \_ для \_ инициализации общего ресурса**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5be42-126"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="5be42-127">Разрешить клиенту инициировать запуск приложения, если он уже выполняется в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="5be42-127">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="5be42-128"><dt>**Ндде \_ ДОВЕРЕНный \_ общий ресурс \_ Start**</dt> <dt>0x80000000L</dt></span><span class="sxs-lookup"><span data-stu-id="5be42-128"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="5be42-129">Разрешить запуск приложения в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="5be42-129">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="5be42-130">*lpdwShareModId0* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5be42-130">*lpdwShareModId0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5be42-131">Указатель на переменную, которая получает первую часть идентификатора изменения доверенного общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="5be42-131">A pointer to a variable that receives the first part of the trusted share modify identifier.</span></span> <span data-ttu-id="5be42-132">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5be42-132">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5be42-133">*lpdwShareModId1* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5be42-133">*lpdwShareModId1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5be42-134">Указатель на переменную, которая получает вторую часть идентификатора изменения доверенного общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="5be42-134">A pointer to a variable that receives the second part of the trusted share modify identifier.</span></span> <span data-ttu-id="5be42-135">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5be42-135">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5be42-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5be42-136">Return value</span></span>

<span data-ttu-id="5be42-137">Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="5be42-137">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="5be42-138">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="5be42-138">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5be42-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5be42-139">Remarks</span></span>

<span data-ttu-id="5be42-140">Идентификатор изменения доверенного общего ресурса отражает версию общего ресурса DDE в DSDM на момент, когда общий ресурс DDE изначально получил состояние Trusted.</span><span class="sxs-lookup"><span data-stu-id="5be42-140">The trusted share modify identifier reflects the version of the DDE share in the DSDM at the time the DDE share was initially granted trusted status.</span></span> <span data-ttu-id="5be42-141">Идентификатор изменения доверенного общего ресурса в основном используется для удаления устаревших доверенных общих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5be42-141">The trusted share modify identifier is primarily used to remove obsolete trusted shares.</span></span> <span data-ttu-id="5be42-142">Однако пользователю не нужно удалять устаревшие доверенные общие папки.</span><span class="sxs-lookup"><span data-stu-id="5be42-142">However, the user does not need to remove obsolete trusted shares.</span></span> <span data-ttu-id="5be42-143">Агент сетевого DDE удаляет устаревшие общие папки от имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="5be42-143">The network DDE agent removes obsolete shares on the user's behalf.</span></span>

## <a name="requirements"></a><span data-ttu-id="5be42-144">Требования</span><span class="sxs-lookup"><span data-stu-id="5be42-144">Requirements</span></span>



| <span data-ttu-id="5be42-145">Требование</span><span class="sxs-lookup"><span data-stu-id="5be42-145">Requirement</span></span> | <span data-ttu-id="5be42-146">Значение</span><span class="sxs-lookup"><span data-stu-id="5be42-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5be42-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5be42-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5be42-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5be42-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5be42-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5be42-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5be42-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5be42-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5be42-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5be42-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="5be42-152"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5be42-152"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="5be42-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5be42-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="5be42-154"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5be42-154"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5be42-155">DLL</span><span class="sxs-lookup"><span data-stu-id="5be42-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5be42-156"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5be42-156"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="5be42-157">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="5be42-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5be42-158">**Нддежеттрустедшарев** (Юникод) и **нддежеттрустедшареа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5be42-158">**NDdeGetTrustedShareW** (Unicode) and **NDdeGetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="5be42-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5be42-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be42-160">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="5be42-160">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="5be42-161">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="5be42-161">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="5be42-162">**нддесеттрустедшаре**</span><span class="sxs-lookup"><span data-stu-id="5be42-162">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

 




