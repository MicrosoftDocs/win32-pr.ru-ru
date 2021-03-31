---
title: Функция Вмкреатестреамфорурл
description: Функция Вмкреатестреамфорурл реализуется приложением для создания объекта COM IStream для данного URL-адреса.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Вмкреатестреамфорурл функция Windows Media Format
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411851"
---
# <a name="wmcreatestreamforurl-function"></a><span data-ttu-id="5dac7-104">Функция Вмкреатестреамфорурл</span><span class="sxs-lookup"><span data-stu-id="5dac7-104">WMCreateStreamForURL function</span></span>

<span data-ttu-id="5dac7-105">Функция **вмкреатестреамфорурл** реализуется приложением для создания объекта COM **IStream** для данного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5dac7-105">The **WMCreateStreamForURL** function is implemented by the application to create a COM **IStream** object for a given URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dac7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dac7-106">Syntax</span></span>


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a><span data-ttu-id="5dac7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dac7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dac7-108">*пвсзурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5dac7-108">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dac7-109">Указатель на строку расширенных символов, содержащую URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5dac7-109">Pointer to a wide-character string containing the URL.</span></span>

</dd> <dt>

<span data-ttu-id="5dac7-110">*пфкорректсаурце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5dac7-110">*pfCorrectSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dac7-111">Указатель на флаг, true запрещает пакету SDK пытаться выполнять другие подключаемые модули источника для этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5dac7-111">Pointer to a flag, true will prevent the SDK from trying other source plug-ins for this URL.</span></span>

</dd> <dt>

<span data-ttu-id="5dac7-112">*ппстреам* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5dac7-112">*ppStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dac7-113">Указатель на указатель на объект **IStream** , созданный методом.</span><span class="sxs-lookup"><span data-stu-id="5dac7-113">Pointer to a pointer to the **IStream** object created by the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dac7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dac7-114">Return value</span></span>

<span data-ttu-id="5dac7-115">Если функция выполнена успешно, она должна вернуть значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5dac7-115">If the function succeeds, it must return S\_OK.</span></span> <span data-ttu-id="5dac7-116">В случае сбоя он должен вернуть соответствующий код ошибки **HRESULT** , а \* *Ппстреам* должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="5dac7-116">If it fails, it must return an appropriate **HRESULT** error code, and \**ppStream* should be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="5dac7-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dac7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dac7-118">**Подключаемые модули источника**</span><span class="sxs-lookup"><span data-stu-id="5dac7-118">**Source Plug-ins**</span></span>](source-plug-ins.md)
</dt> </dl>

 

 




