---
description: Отключает функции.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: Функция Псетупсетглобалфлагс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649046"
---
# <a name="psetupsetglobalflags-function"></a><span data-ttu-id="34739-103">Функция Псетупсетглобалфлагс</span><span class="sxs-lookup"><span data-stu-id="34739-103">pSetupSetGlobalFlags function</span></span>

<span data-ttu-id="34739-104">\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="34739-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="34739-105">Отключает функции.</span><span class="sxs-lookup"><span data-stu-id="34739-105">Disables features.</span></span>

## <a name="syntax"></a><span data-ttu-id="34739-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34739-106">Syntax</span></span>


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="34739-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34739-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34739-108">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34739-108">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34739-109">Флаги, используемые для отключения пользовательского интерфейса или автоматического резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="34739-109">The flags used to disable user interface or automatic backup.</span></span>



| <span data-ttu-id="34739-110">Значение</span><span class="sxs-lookup"><span data-stu-id="34739-110">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="34739-111">Значение</span><span class="sxs-lookup"><span data-stu-id="34739-111">Meaning</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <span data-ttu-id="34739-112"><dt>**Пспгф \_ Неинтерактивный**</dt> <dt>0x004</dt></span><span class="sxs-lookup"><span data-stu-id="34739-112"><dt>**PSPGF\_NONINTERACTIVE**</dt> <dt>0x004</dt></span></span> </dl> | <span data-ttu-id="34739-113">Установите для отключения интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="34739-113">Set to disable user interface.</span></span><br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <span data-ttu-id="34739-114"><dt>**Пспгф \_ НЕТ \_ резервной копии**</dt> <dt>0x002</dt></span><span class="sxs-lookup"><span data-stu-id="34739-114"><dt>**PSPGF\_NO\_BACKUP**</dt> <dt>0x002</dt></span></span> </dl>               | <span data-ttu-id="34739-115">Установите для отключения автоматической архивации.</span><span class="sxs-lookup"><span data-stu-id="34739-115">Set to disable automatic backup.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34739-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34739-116">Return value</span></span>

<span data-ttu-id="34739-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="34739-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34739-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34739-118">Remarks</span></span>

<span data-ttu-id="34739-119">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="34739-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="34739-120">Требования</span><span class="sxs-lookup"><span data-stu-id="34739-120">Requirements</span></span>



| <span data-ttu-id="34739-121">Требование</span><span class="sxs-lookup"><span data-stu-id="34739-121">Requirement</span></span> | <span data-ttu-id="34739-122">Значение</span><span class="sxs-lookup"><span data-stu-id="34739-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34739-123">DLL</span><span class="sxs-lookup"><span data-stu-id="34739-123">DLL</span></span><br/> | <dl> <span data-ttu-id="34739-124"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34739-124"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
