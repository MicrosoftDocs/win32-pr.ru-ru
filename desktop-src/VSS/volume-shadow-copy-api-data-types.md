---
description: 'В API теневого копирования томов определены следующие типы данных:'
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Типы данных API теневого копирования томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809838"
---
# <a name="volume-shadow-copy-api-data-types"></a><span data-ttu-id="37475-103">Типы данных API теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="37475-103">Volume Shadow Copy API Data Types</span></span>

<span data-ttu-id="37475-104">В API теневого копирования томов определены следующие типы данных:</span><span class="sxs-lookup"><span data-stu-id="37475-104">The following data types are defined in the Volume Shadow Copy API:</span></span>

<dl> <dt>

<span data-ttu-id="37475-105"><span id="VSS_ID"></span><span id="vss_id"></span>\_идентификатор VSS</span><span class="sxs-lookup"><span data-stu-id="37475-105"><span id="VSS_ID"></span><span id="vss_id"></span>VSS\_ID</span></span>
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

<span data-ttu-id="37475-106">Определение **\_ идентификатора VSS** указывает общий формат идентификатора VSS.</span><span class="sxs-lookup"><span data-stu-id="37475-106">The **VSS\_ID** definition specifies the general VSS identifier format.</span></span> <span data-ttu-id="37475-107">**\_ Идентификатор VSS** является стандартным типом данных GUID.</span><span class="sxs-lookup"><span data-stu-id="37475-107">The **VSS\_ID** is a standard GUID data type.</span></span>

<span data-ttu-id="37475-108">Служба **VSS \_ ИДЕНТИФИКАТОРы** используются для идентификации следующих объектов: теневые копии, наборы теневых копий, поставщики, версии поставщиков, модули записи (идентификатор класса модуля записи) и экземпляры модулей записи.</span><span class="sxs-lookup"><span data-stu-id="37475-108">**VSS\_ID** s are used to identify the following: shadow copies, shadow copy sets, providers, provider versions, writers (writer's class identifier), and instances of writers.</span></span>

</dd> <dt>

<span data-ttu-id="37475-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>\_ПВСЗ VSS</span><span class="sxs-lookup"><span data-stu-id="37475-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS\_PWSZ</span></span>
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

<span data-ttu-id="37475-110">Определение **\_ Пвсз для VSS** указывает строку расширенных символов, заканчивающуюся нулем (WChar).</span><span class="sxs-lookup"><span data-stu-id="37475-110">The **VSS\_PWSZ** definition specifies a null-terminated wide character string (wchar).</span></span>

</dd> <dt>

<span data-ttu-id="37475-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>\_Метка времени VSS</span><span class="sxs-lookup"><span data-stu-id="37475-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS\_TIMESTAMP</span></span>
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

<span data-ttu-id="37475-112">Определение **\_ метки времени VSS** содержит сведения о временной метке в виде 64-разрядного целого числа, содержащего число 100-наносекундных интервалов, прошедших с 1 января 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="37475-112">The **VSS\_TIMESTAMP** definition holds time-stamp information as a 64-bit integer value containing the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="37475-113">Это определение является взаимозаменяемым с структурой [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="37475-113">This definition is interchangeable with the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> </dl>

 

 
