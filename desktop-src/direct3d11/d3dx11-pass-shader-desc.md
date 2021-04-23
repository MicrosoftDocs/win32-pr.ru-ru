---
title: Структура D3DX11_PASS_SHADER_DESC (D3dx11effect. h)
description: Описывает пройденный результат.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987200"
---
# <a name="d3dx11_pass_shader_desc-structure"></a><span data-ttu-id="e3f33-104">\_ \_ Структура построителя шейдеров D3DX11 Pass \_</span><span class="sxs-lookup"><span data-stu-id="e3f33-104">D3DX11\_PASS\_SHADER\_DESC structure</span></span>

<span data-ttu-id="e3f33-105">Описывает пройденный результат.</span><span class="sxs-lookup"><span data-stu-id="e3f33-105">Describes an effect pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f33-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3f33-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="e3f33-107">Участники</span><span class="sxs-lookup"><span data-stu-id="e3f33-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3f33-108">**пшадервариабле**</span><span class="sxs-lookup"><span data-stu-id="e3f33-108">**pShaderVariable**</span></span>
</dt> <dd>

<span data-ttu-id="e3f33-109">Тип: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3f33-109">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="e3f33-110">Переменная, из которой получен этот шейдер.</span><span class="sxs-lookup"><span data-stu-id="e3f33-110">The variable that this shader came from.</span></span>

</dd> <dt>

<span data-ttu-id="e3f33-111">**шадериндекс**</span><span class="sxs-lookup"><span data-stu-id="e3f33-111">**ShaderIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e3f33-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e3f33-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e3f33-113">Элемент Пшадервариабле (если массив) или 0, если не применимо.</span><span class="sxs-lookup"><span data-stu-id="e3f33-113">The element of pShaderVariable (if an array) or 0 if not applicable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3f33-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3f33-114">Remarks</span></span>

<span data-ttu-id="e3f33-115">D3DX11 \_ Pass \_ Shader \_ DESC используется с методами [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* шадердеск.</span><span class="sxs-lookup"><span data-stu-id="e3f33-115">D3DX11\_PASS\_SHADER\_DESC is used with [**ID3DX11EffectPass**](id3dx11effectpass.md) Get\*ShaderDesc methods.</span></span>

<span data-ttu-id="e3f33-116">Если это назначение встроенного шейдера, возвращаемым интерфейсом будет анонимная переменная шейдера, которая не может быть извлечена другим способом.</span><span class="sxs-lookup"><span data-stu-id="e3f33-116">If this is an inline shader assignment, the returned interface will be an anonymous shader variable, which is not retrievable any other way.</span></span> <span data-ttu-id="e3f33-117">Его имя в описании переменной будет «$Anonymous».</span><span class="sxs-lookup"><span data-stu-id="e3f33-117">It's name in the variable description will be "$Anonymous".</span></span> <span data-ttu-id="e3f33-118">Если в блоке Pass нет назначения этого типа, Пшадервариабле! = **null**, но пшадервариабле->IsValid () = = **false**.</span><span class="sxs-lookup"><span data-stu-id="e3f33-118">If there is no assignment of this type in the pass block, pShaderVariable != **NULL**, but pShaderVariable->IsValid() == **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f33-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e3f33-119">Requirements</span></span>



| <span data-ttu-id="e3f33-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e3f33-120">Requirement</span></span> | <span data-ttu-id="e3f33-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e3f33-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f33-122">Header</span><span class="sxs-lookup"><span data-stu-id="e3f33-122">Header</span></span><br/> | <dl> <span data-ttu-id="e3f33-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f33-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3f33-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3f33-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f33-125">Эффекты с 11 по структурам</span><span class="sxs-lookup"><span data-stu-id="e3f33-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

