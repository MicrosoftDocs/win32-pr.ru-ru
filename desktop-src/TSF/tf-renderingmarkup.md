---
title: Структура TF_RENDERINGMARKUP
description: '\_Структура структуры TF рендерингмаркуп содержит диапазон и сведения об атрибуте вывода.'
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- Инфраструктура текстовых служб TF_RENDERINGMARKUP Structure
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105681530"
---
# <a name="tf_renderingmarkup-structure"></a><span data-ttu-id="57fad-104">\_Структура TF рендерингмаркуп</span><span class="sxs-lookup"><span data-stu-id="57fad-104">TF\_RENDERINGMARKUP structure</span></span>

<span data-ttu-id="57fad-105">Структура структуры [**tf \_ рендерингмаркуп**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) содержит диапазон и сведения об атрибуте вывода.</span><span class="sxs-lookup"><span data-stu-id="57fad-105">The [**TF\_RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) structure structure contains a range and the display attribute information.</span></span>

## <a name="syntax"></a><span data-ttu-id="57fad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57fad-106">Syntax</span></span>


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a><span data-ttu-id="57fad-107">Члены</span><span class="sxs-lookup"><span data-stu-id="57fad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="57fad-108">**пранже**</span><span class="sxs-lookup"><span data-stu-id="57fad-108">**pRange**</span></span>
</dt> <dd>

<span data-ttu-id="57fad-109">Указатель на интерфейс [итфранже](/windows/desktop/api/Msctf/nn-msctf-itfrange) .</span><span class="sxs-lookup"><span data-stu-id="57fad-109">A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface.</span></span>

</dd> <dt>

<span data-ttu-id="57fad-110">**тфдисплайаттр**</span><span class="sxs-lookup"><span data-stu-id="57fad-110">**tfDisplayAttr**</span></span>
</dt> <dd>

<span data-ttu-id="57fad-111">Отображение сведений об атрибутах.</span><span class="sxs-lookup"><span data-stu-id="57fad-111">Display attribute information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57fad-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57fad-112">Remarks</span></span>

<span data-ttu-id="57fad-113">Эта структура в настоящий момент не находится в файлах общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="57fad-113">This structure is not currently in the public header files.</span></span> <span data-ttu-id="57fad-114">Чтобы использовать этот API, необходимо скомпилировать [прототип](prototypes.md)с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="57fad-114">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 




