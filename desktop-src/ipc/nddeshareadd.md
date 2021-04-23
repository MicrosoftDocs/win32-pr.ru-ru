---
description: Создает и добавляет новый общий ресурс DDE в диспетчер общей базы данных DDE (DSDM).
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Функция Нддешареадд (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684210"
---
# <a name="nddeshareadd-function"></a><span data-ttu-id="19cc8-103">Функция Нддешареадд</span><span class="sxs-lookup"><span data-stu-id="19cc8-103">NDdeShareAdd function</span></span>

<span data-ttu-id="19cc8-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="19cc8-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="19cc8-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="19cc8-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="19cc8-106">Создает и добавляет новый общий ресурс DDE в диспетчер общей базы данных DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="19cc8-106">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="19cc8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19cc8-107">Syntax</span></span>


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="19cc8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="19cc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19cc8-109">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19cc8-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cc8-110">Имя сервера, DSDM которого необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="19cc8-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="19cc8-111">*нлевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19cc8-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cc8-112">Уровень информации.</span><span class="sxs-lookup"><span data-stu-id="19cc8-112">The information level.</span></span> <span data-ttu-id="19cc8-113">Этот параметр должен быть равен 2.</span><span class="sxs-lookup"><span data-stu-id="19cc8-113">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="19cc8-114">*pSD* \[ - окне\]</span><span class="sxs-lookup"><span data-stu-id="19cc8-114">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cc8-115">Указатель на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , которая должна быть связана с этой общей папкой, и какие проверки доступа будут выполняться при последующих инициациях для этой общей папки.</span><span class="sxs-lookup"><span data-stu-id="19cc8-115">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure to be associated with this share and against which access checks will be performed on subsequent initiates to this share.</span></span> <span data-ttu-id="19cc8-116">Этот параметр может иметь **значение NULL**. в этом случае DSDM создает дескриптор безопасности по умолчанию, который предоставляет владельцу разрешение «Полный доступ» и «чтение и связывание» для всех.</span><span class="sxs-lookup"><span data-stu-id="19cc8-116">This parameter can be **NULL**, in which case the DSDM creates a default security descriptor that grants "Full Control" to the owner and "Read and Link" to everyone.</span></span>

</dd> <dt>

<span data-ttu-id="19cc8-117">*lpBuffer* \[ввод\]</span><span class="sxs-lookup"><span data-stu-id="19cc8-117">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cc8-118">Указатель на структуру [**нддешареинфо**](nddeshareinfo-str.md) , определяющую список аппликатионтопик, связанный с создаваемым общим РЕСУРСом DDE, а также другими параметрами.</span><span class="sxs-lookup"><span data-stu-id="19cc8-118">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that defines the ApplicationTopic list associated with the DDE share being created as well as other parameters.</span></span> <span data-ttu-id="19cc8-119">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="19cc8-119">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19cc8-120">*кбуфсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19cc8-120">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cc8-121">Размер структуры *лпбуффер* в байтах.</span><span class="sxs-lookup"><span data-stu-id="19cc8-121">The size of the *lpBuffer* structure, in bytes.</span></span> <span data-ttu-id="19cc8-122">Этот параметр не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="19cc8-122">This parameter cannot be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19cc8-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19cc8-123">Return value</span></span>

<span data-ttu-id="19cc8-124">Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="19cc8-124">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="19cc8-125">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="19cc8-125">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="19cc8-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19cc8-126">Remarks</span></span>

<span data-ttu-id="19cc8-127">Прежде чем клиент сможет подключиться к общему ресурсу DDE, он должен быть доверенным для [**нддесеттрустедшаре**](nddesettrustedshare.md).</span><span class="sxs-lookup"><span data-stu-id="19cc8-127">Before a client can connect to the DDE share, it must be trusted with [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19cc8-128">Требования</span><span class="sxs-lookup"><span data-stu-id="19cc8-128">Requirements</span></span>



| <span data-ttu-id="19cc8-129">Требование</span><span class="sxs-lookup"><span data-stu-id="19cc8-129">Requirement</span></span> | <span data-ttu-id="19cc8-130">Значение</span><span class="sxs-lookup"><span data-stu-id="19cc8-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19cc8-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19cc8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="19cc8-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19cc8-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="19cc8-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19cc8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="19cc8-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19cc8-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="19cc8-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="19cc8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="19cc8-136"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="19cc8-136"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="19cc8-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="19cc8-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="19cc8-138"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19cc8-138"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="19cc8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="19cc8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19cc8-140"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19cc8-140"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="19cc8-141">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="19cc8-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="19cc8-142">**Нддешареаддв** (Юникод) и **нддешареадда** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="19cc8-142">**NDdeShareAddW** (Unicode) and **NDdeShareAddA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="19cc8-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19cc8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19cc8-144">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="19cc8-144">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="19cc8-145">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="19cc8-145">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="19cc8-146">**нддешареинфо**</span><span class="sxs-lookup"><span data-stu-id="19cc8-146">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="19cc8-147">**нддесеттрустедшаре**</span><span class="sxs-lookup"><span data-stu-id="19cc8-147">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

