---
description: Инициализирует необязательный Диспетчер компонентов.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: Функция ОЦинитиализе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648061"
---
# <a name="ocinitialize-function"></a><span data-ttu-id="3c104-103">Функция ОЦинитиализе</span><span class="sxs-lookup"><span data-stu-id="3c104-103">OcInitialize function</span></span>

<span data-ttu-id="3c104-104">Инициализирует необязательный Диспетчер компонентов.</span><span class="sxs-lookup"><span data-stu-id="3c104-104">Initializes the optional component manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c104-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c104-105">Syntax</span></span>


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a><span data-ttu-id="3c104-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c104-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c104-107">*Обратные вызовы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c104-107">*Callbacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c104-108">Указатель на структуру [**\_ \_ обратных вызовов клиента OCM**](ocm-client-callbacks.md) , указывающий функции обратного вызова, которые используются диспетчером OC для выполнения различных задач.</span><span class="sxs-lookup"><span data-stu-id="3c104-108">A pointer to an [**OCM\_CLIENT\_CALLBACKS**](ocm-client-callbacks.md) structure that specifies the callback functions to be used by the OC manager to perform various tasks.</span></span>

</dd> <dt>

<span data-ttu-id="3c104-109">*МастероЦинфнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c104-109">*MasterOcInfName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c104-110">Путь к главному файлу OC. INF.</span><span class="sxs-lookup"><span data-stu-id="3c104-110">The path of the master OC .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="3c104-111">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c104-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c104-112">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3c104-112">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3c104-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**ОЦинит \_ ФОРЦЕНЕВИНФ** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="3c104-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT\_FORCENEWINF** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="3c104-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**ОЦинит \_ КИЛЛСУБКОМПС** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="3c104-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT\_KILLSUBCOMPS** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="3c104-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**ОЦинит \_ РУНКУИЕТ** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="3c104-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT\_RUNQUIET** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="3c104-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**ОЦинит \_ ЛАНГУАЖЕАВАРЕ** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="3c104-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT\_LANGUAGEAWARE** (0x00000008)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3c104-117">*ShowError* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3c104-117">*ShowError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c104-118">Если функция завершается ошибкой, этот параметр указывает, следует ли отображать сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3c104-118">If the function fails, this parameter indicates whether to display an error message.</span></span>

</dd> <dt>

<span data-ttu-id="3c104-119">*Журнал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c104-119">*Log* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c104-120">Маркер журнала.</span><span class="sxs-lookup"><span data-stu-id="3c104-120">A handle to the log.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c104-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c104-121">Return value</span></span>

<span data-ttu-id="3c104-122">Функция возвращает значение контекста для диспетчера OC.</span><span class="sxs-lookup"><span data-stu-id="3c104-122">The function returns the OC manager context value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c104-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c104-123">Remarks</span></span>

<span data-ttu-id="3c104-124">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3c104-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c104-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3c104-125">Requirements</span></span>



| <span data-ttu-id="3c104-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3c104-126">Requirement</span></span> | <span data-ttu-id="3c104-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3c104-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c104-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3c104-128">DLL</span></span><br/> | <dl> <span data-ttu-id="3c104-129"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c104-129"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c104-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c104-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c104-131">**\_ \_ обратные вызовы клиента OCM**</span><span class="sxs-lookup"><span data-stu-id="3c104-131">**OCM\_CLIENT\_CALLBACKS**</span></span>](ocm-client-callbacks.md)
</dt> <dt>

[<span data-ttu-id="3c104-132">**октерминате**</span><span class="sxs-lookup"><span data-stu-id="3c104-132">**OcTerminate**</span></span>](octerminate.md)
</dt> </dl>

 

 
