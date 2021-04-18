---
description: В PStore используются следующие константы.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Константы PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668539"
---
# <a name="pstore-constants"></a><span data-ttu-id="4151d-103">Константы PStore</span><span class="sxs-lookup"><span data-stu-id="4151d-103">PStore Constants</span></span>

<span data-ttu-id="4151d-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4151d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4151d-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="4151d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4151d-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="4151d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4151d-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="4151d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4151d-108">В PStore используются следующие константы.</span><span class="sxs-lookup"><span data-stu-id="4151d-108">The following constants are used by PStore.</span></span>

<span data-ttu-id="4151d-109">Коды ошибок защищенного хранилища</span><span class="sxs-lookup"><span data-stu-id="4151d-109">Protected Storage Error Codes</span></span>



| <span data-ttu-id="4151d-110">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="4151d-110">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="4151d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4151d-111">Description</span></span>                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <span data-ttu-id="4151d-112">PST-файл <dt>**\_ E \_**</dt> ! <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="4151d-112"><dt>**PST\_E\_OK**</dt> <dt>0x00000000L</dt></span></span> </dl>                             | <span data-ttu-id="4151d-113">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4151d-113">The operation was successful.</span></span><br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <span data-ttu-id="4151d-114">PST-файл <dt>**\_ \_Тип E \_ существует**</dt> <dt>0x800C0004L</dt></span><span class="sxs-lookup"><span data-stu-id="4151d-114"><dt>**PST\_E\_TYPE\_EXISTS**</dt> <dt>0x800C0004L</dt></span></span> </dl> | <span data-ttu-id="4151d-115">Элемент данных уже существует в защищенном хранилище.</span><span class="sxs-lookup"><span data-stu-id="4151d-115">The data item already exists in the protected storage.</span></span> <br/> |



<span data-ttu-id="4151d-116">Значения предложения Access</span><span class="sxs-lookup"><span data-stu-id="4151d-116">Access Clause Values</span></span>



| <span data-ttu-id="4151d-117">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="4151d-117">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="4151d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4151d-118">Description</span></span>                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <span data-ttu-id="4151d-119">PST-файл <dt>**\_ AUTHENTICODE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4151d-119"><dt>**PST\_AUTHENTICODE**</dt> <dt>1</dt></span></span> </dl>                       | <span data-ttu-id="4151d-120">Указывает на структуру [**PST \_ аусентикодедата**](pst-authenticodedata.md) .</span><span class="sxs-lookup"><span data-stu-id="4151d-120">Points to a [**PST\_AUTHENTICODEDATA**](pst-authenticodedata.md) structure.</span></span><br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <span data-ttu-id="4151d-121"><dt> **\_ Двоичная \_ Проверка PST**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4151d-121"><dt>**PST\_BINARY\_CHECK** </dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="4151d-122">Указывает на структуру **PST \_ бинаричеккдата** .</span><span class="sxs-lookup"><span data-stu-id="4151d-122">Points to a **PST\_BINARYCHECKDATA** structure.</span></span><br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <span data-ttu-id="4151d-123">PST-файл <dt>**\_ \_Дескриптор безопасности**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4151d-123"><dt>**PST\_SECURITY\_DESCRIPTOR**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="4151d-124">Указывает на допустимый дескриптор безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="4151d-124">Points to a valid Windows security descriptor.</span></span> <br/>                              |



## <a name="requirements"></a><span data-ttu-id="4151d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4151d-125">Requirements</span></span>



| <span data-ttu-id="4151d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4151d-126">Requirement</span></span> | <span data-ttu-id="4151d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4151d-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4151d-128">Header</span><span class="sxs-lookup"><span data-stu-id="4151d-128">Header</span></span><br/> | <dl> <span data-ttu-id="4151d-129"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="4151d-129"><dt>Pstore.h</dt></span></span> </dl> |



 

 
