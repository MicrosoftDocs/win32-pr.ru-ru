---
description: Возвращает объект перечислителя, который можно использовать, в свою очередь, для перечисления поставщиков защищенного хранилища, установленных в данный момент в системе.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Функция Псторинумпровидерс (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648914"
---
# <a name="pstoreenumproviders-function"></a><span data-ttu-id="522e2-103">Функция Псторинумпровидерс</span><span class="sxs-lookup"><span data-stu-id="522e2-103">PStoreEnumProviders function</span></span>

<span data-ttu-id="522e2-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="522e2-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="522e2-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="522e2-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="522e2-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="522e2-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="522e2-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="522e2-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="522e2-108">Возвращает объект перечислителя, который можно использовать, в свою очередь, для перечисления поставщиков защищенного хранилища, установленных в данный момент в системе.</span><span class="sxs-lookup"><span data-stu-id="522e2-108">Gets an enumerator object that can be used in turn to enumerate the protected storage providers that are currently installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="522e2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="522e2-109">Syntax</span></span>


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="522e2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="522e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="522e2-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="522e2-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="522e2-112">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="522e2-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="522e2-113">*ппенум*</span><span class="sxs-lookup"><span data-stu-id="522e2-113">*ppenum*</span></span> 
</dt> <dd>

<span data-ttu-id="522e2-114">Указатель на указатель на интерфейс [**иенумпсторепровидерс**](ienumpstoreproviders.md) , который может использоваться для перечисления установленных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="522e2-114">A pointer to a pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) interface that can be used to enumerate installed providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="522e2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="522e2-115">Return value</span></span>

<span data-ttu-id="522e2-116">Эта функция возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="522e2-116">This function returns an **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="522e2-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="522e2-117">Remarks</span></span>

<span data-ttu-id="522e2-118">Компонент защищенного хранилища имеет архитектуру на основе поставщика.</span><span class="sxs-lookup"><span data-stu-id="522e2-118">The protected storage component has a provider-based architecture.</span></span> <span data-ttu-id="522e2-119">Приложения, использующие защищенное хранилище, могут указывать, какой из установленных поставщиков следует использовать при хранении и извлечении данных.</span><span class="sxs-lookup"><span data-stu-id="522e2-119">Applications that make use of protected storage can specify which of the installed providers to use when storing and retrieving their data.</span></span>

<span data-ttu-id="522e2-120">Функция **псторинумпровидерс** используется для перечисления установленных поставщиков защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="522e2-120">The **PStoreEnumProviders** function is used to enumerate the installed protected storage providers.</span></span> <span data-ttu-id="522e2-121">Каждый поставщик идентифицируется по глобальному уникальному идентификатору (GUID).</span><span class="sxs-lookup"><span data-stu-id="522e2-121">Each provider is identified by a globally unique identifier (GUID).</span></span>

<span data-ttu-id="522e2-122">До этого времени только один поставщик защищенного хранилища когда-либо записался.</span><span class="sxs-lookup"><span data-stu-id="522e2-122">Up to this time, only one protected storage provider has ever been written.</span></span> <span data-ttu-id="522e2-123">Учитывая, что служба защищенного хранилища в настоящее время устарела, очень маловероятно, что все дополнительные поставщики будут созданы.</span><span class="sxs-lookup"><span data-stu-id="522e2-123">Given that the protected storage service is currently deprecated, it is very unlikely that any additional providers will ever be produced.</span></span> <span data-ttu-id="522e2-124">В результате эта функция не должна использоваться ни в каких целях.</span><span class="sxs-lookup"><span data-stu-id="522e2-124">As a result, this function should not be used for any purpose.</span></span>

<span data-ttu-id="522e2-125">Эта функция не имеет связанной библиотеки импорта; его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="522e2-125">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="522e2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="522e2-126">Requirements</span></span>



| <span data-ttu-id="522e2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="522e2-127">Requirement</span></span> | <span data-ttu-id="522e2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="522e2-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="522e2-129">Header</span><span class="sxs-lookup"><span data-stu-id="522e2-129">Header</span></span><br/> | <dl> <span data-ttu-id="522e2-130"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="522e2-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="522e2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="522e2-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="522e2-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="522e2-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="522e2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="522e2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522e2-134">**иенумпсторепровидерс**</span><span class="sxs-lookup"><span data-stu-id="522e2-134">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
