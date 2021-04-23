---
description: Атрибут — это пара "ключ-значение", в которой ключ является идентификатором GUID, а значение — ПРОПВАРИАНТ. Атрибуты используются в Microsoft Media Foundation для настройки объектов, описания форматов мультимедиа, свойств объектов запросов и других целей.
ms.assetid: 44af5e03-5f0a-4564-b9d6-b8c935df35b2
title: Атрибуты в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e7893586aa1e966b95c1af5d04246bbb0c82ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808188"
---
# <a name="attributes-in-media-foundation"></a><span data-ttu-id="47030-104">Атрибуты в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="47030-104">Attributes in Media Foundation</span></span>

<span data-ttu-id="47030-105">Атрибут — это пара "ключ-значение", в которой ключ является идентификатором GUID, а значение — **пропвариант**.</span><span class="sxs-lookup"><span data-stu-id="47030-105">An attribute is a key/value pair, where the key is a GUID and the value is a **PROPVARIANT**.</span></span> <span data-ttu-id="47030-106">Атрибуты используются в Microsoft Media Foundation для настройки объектов, описания форматов мультимедиа, свойств объектов запросов и других целей.</span><span class="sxs-lookup"><span data-stu-id="47030-106">Attributes are used throughout Microsoft Media Foundation to configure objects, describe media formats, query object properties, and other purposes.</span></span>

<span data-ttu-id="47030-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="47030-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="47030-108">Общие сведения об атрибутах</span><span class="sxs-lookup"><span data-stu-id="47030-108">About Attributes</span></span>](#about-attributes)
-   [<span data-ttu-id="47030-109">Сериализация атрибутов</span><span class="sxs-lookup"><span data-stu-id="47030-109">Serializing Attributes</span></span>](#serializing-attributes)
-   [<span data-ttu-id="47030-110">Реализация Имфаттрибутес</span><span class="sxs-lookup"><span data-stu-id="47030-110">Implementing IMFAttributes</span></span>](#implementing-imfattributes)
-   [<span data-ttu-id="47030-111">См. также</span><span class="sxs-lookup"><span data-stu-id="47030-111">Related topics</span></span>](#related-topics)

## <a name="about-attributes"></a><span data-ttu-id="47030-112">Общие сведения об атрибутах</span><span class="sxs-lookup"><span data-stu-id="47030-112">About Attributes</span></span>

<span data-ttu-id="47030-113">Атрибут — это пара "ключ-значение", в которой ключ является идентификатором GUID, а значение — **пропвариант**.</span><span class="sxs-lookup"><span data-stu-id="47030-113">An attribute is a key/value pair, where the key is a GUID and the value is a **PROPVARIANT**.</span></span> <span data-ttu-id="47030-114">Значения атрибутов ограничены следующими типами данных:</span><span class="sxs-lookup"><span data-stu-id="47030-114">Attribute values are restricted to the following data types:</span></span>

-   <span data-ttu-id="47030-115">32-разрядное целое число без знака (**UINT32**).</span><span class="sxs-lookup"><span data-stu-id="47030-115">Unsigned 32-bit integer (**UINT32**).</span></span>
-   <span data-ttu-id="47030-116">64-разрядное целое число без знака (**UINT64**).</span><span class="sxs-lookup"><span data-stu-id="47030-116">Unsigned 64-bit integer (**UINT64**).</span></span>
-   <span data-ttu-id="47030-117">64-разрядное число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="47030-117">64-bit floating-point number.</span></span>
-   <span data-ttu-id="47030-118">GUID.</span><span class="sxs-lookup"><span data-stu-id="47030-118">GUID.</span></span>
-   <span data-ttu-id="47030-119">Строка расширенных символов, заканчивающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="47030-119">Null-terminated wide-character string.</span></span>
-   <span data-ttu-id="47030-120">Массив байтов.</span><span class="sxs-lookup"><span data-stu-id="47030-120">Byte array.</span></span>
-   <span data-ttu-id="47030-121">Указатель **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="47030-121">**IUnknown** pointer.</span></span>

<span data-ttu-id="47030-122">Эти типы определяются в перечислении [**\_ \_ типа атрибута MF**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) .</span><span class="sxs-lookup"><span data-stu-id="47030-122">These types are defined in the [**MF\_ATTRIBUTE\_TYPE**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) enumeration.</span></span> <span data-ttu-id="47030-123">Чтобы задать или получить значения атрибутов, используйте интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="47030-123">To set or retrieve attribute values, use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="47030-124">Этот интерфейс содержит строго типизированные методы для получения и задания значений по типу данных.</span><span class="sxs-lookup"><span data-stu-id="47030-124">This interface contains type-safe methods to get and set values by data type.</span></span> <span data-ttu-id="47030-125">Например, чтобы установить 32-разрядное целое число, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="47030-125">For example, to set a 32-bit integer, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span> <span data-ttu-id="47030-126">Ключи атрибутов уникальны в пределах объекта.</span><span class="sxs-lookup"><span data-stu-id="47030-126">Attribute keys are unique within an object.</span></span> <span data-ttu-id="47030-127">Если задать два разных значения с одним и тем же ключом, второе значение перезапишет первый.</span><span class="sxs-lookup"><span data-stu-id="47030-127">If you set two different values with the same key, the second value overwrites the first.</span></span>

<span data-ttu-id="47030-128">Несколько Media Foundation интерфейсов наследуют интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="47030-128">Several Media Foundation interfaces inherit the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="47030-129">Объекты, предоставляющие этот интерфейс, имеют необязательные или обязательные атрибуты, которые приложение должно задать для объекта, или иметь атрибуты, которые приложение может извлечь.</span><span class="sxs-lookup"><span data-stu-id="47030-129">Objects that expose this interface have optional or mandatory attributes that the application should set on the object, or have attributes that the application can retrieve.</span></span> <span data-ttu-id="47030-130">Кроме того, некоторые методы и функции принимают указатель **имфаттрибутес** в качестве параметра, который позволяет приложению устанавливать сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="47030-130">Also, some methods and functions take an **IMFAttributes** pointer as a parameter, which enables the application to set configuration information.</span></span> <span data-ttu-id="47030-131">Приложение должно создать хранилище атрибутов для хранения атрибутов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="47030-131">The application must create an attribute store to hold the configuration attributes.</span></span> <span data-ttu-id="47030-132">Чтобы создать пустое хранилище атрибутов, вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="47030-132">To create an empty attribute store, call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>

<span data-ttu-id="47030-133">В следующем коде показаны две функции.</span><span class="sxs-lookup"><span data-stu-id="47030-133">The following code shows two functions.</span></span> <span data-ttu-id="47030-134">Первый создает новое хранилище атрибутов и устанавливает гипотетический атрибут с именем MY \_ с строковым значением.</span><span class="sxs-lookup"><span data-stu-id="47030-134">The first creates a new attribute store and sets a hypothetical attribute named MY\_ATTRIBUTE with a string value.</span></span> <span data-ttu-id="47030-135">Вторая функция получает значение этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="47030-135">The second function retrieves the value of this attribute.</span></span>


```C++
extern const GUID MY_ATTRIBUTE;

HRESULT ShowCreateAttributeStore(IMFAttributes **ppAttributes)
{
    IMFAttributes *pAttributes = NULL;
    const UINT32 cElements = 10;  // Starting size.

    // Create the empty attribute store.
    HRESULT hr = MFCreateAttributes(&pAttributes, cElements);

    // Set the MY_ATTRIBUTE attribute with a string value.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MY_ATTRIBUTE,
            L"This is a string value"
            );
    }

    // Return the IMFAttributes pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }

    SAFE_RELEASE(pAttributes);

    return hr;
}

HRESULT ShowGetAttributes()
{
    IMFAttributes *pAttributes = NULL;
    WCHAR *pwszValue = NULL;
    UINT32 cchLength = 0;

    // Create the attribute store.
    HRESULT hr = ShowCreateAttributeStore(&pAttributes);

    // Get the attribute.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetAllocatedString(
            MY_ATTRIBUTE,
            &pwszValue,
            &cchLength
            );
    }

    CoTaskMemFree(pwszValue);
    SAFE_RELEASE(pAttributes);

    return hr;
}
```



<span data-ttu-id="47030-136">Полный список атрибутов Media Foundation см. в разделе [Media Foundation Attributes](media-foundation-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="47030-136">For a complete list of Media Foundation attributes, see [Media Foundation Attributes](media-foundation-attributes.md).</span></span> <span data-ttu-id="47030-137">Здесь описан ожидаемый тип данных для каждого атрибута.</span><span class="sxs-lookup"><span data-stu-id="47030-137">The expected data type for each attribute is documented there.</span></span>

## <a name="serializing-attributes"></a><span data-ttu-id="47030-138">Сериализация атрибутов</span><span class="sxs-lookup"><span data-stu-id="47030-138">Serializing Attributes</span></span>

<span data-ttu-id="47030-139">Media Foundation содержит две функции для сериализации хранилищ атрибутов.</span><span class="sxs-lookup"><span data-stu-id="47030-139">Media Foundation has two functions for serializing attribute stores.</span></span> <span data-ttu-id="47030-140">Один записывает атрибуты в массив байтов, а другой записывает их в поток, поддерживающий интерфейс **IStream** .</span><span class="sxs-lookup"><span data-stu-id="47030-140">One writes the attributes to a byte array, the other writes them to a stream that supports the **IStream** interface.</span></span> <span data-ttu-id="47030-141">Каждая функция имеет соответствующую функцию, которая загружает данные.</span><span class="sxs-lookup"><span data-stu-id="47030-141">Each function has a corresponding function that loads the data.</span></span>



| <span data-ttu-id="47030-142">Операция</span><span class="sxs-lookup"><span data-stu-id="47030-142">Operation</span></span> | <span data-ttu-id="47030-143">Массив байтов</span><span class="sxs-lookup"><span data-stu-id="47030-143">Byte Array</span></span>                                                   | <span data-ttu-id="47030-144">IStream</span><span class="sxs-lookup"><span data-stu-id="47030-144">IStream</span></span>                                                                        |
|-----------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="47030-145">Сохранить</span><span class="sxs-lookup"><span data-stu-id="47030-145">Save</span></span>      | [<span data-ttu-id="47030-146">**мфжетаттрибутесасблоб**</span><span class="sxs-lookup"><span data-stu-id="47030-146">**MFGetAttributesAsBlob**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob)       | [<span data-ttu-id="47030-147">**мфсериализеаттрибутестостреам**</span><span class="sxs-lookup"><span data-stu-id="47030-147">**MFSerializeAttributesToStream**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream)         |
| <span data-ttu-id="47030-148">Загрузить</span><span class="sxs-lookup"><span data-stu-id="47030-148">Load</span></span>      | [<span data-ttu-id="47030-149">**мфинитаттрибутесфромблоб**</span><span class="sxs-lookup"><span data-stu-id="47030-149">**MFInitAttributesFromBlob**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob) | [<span data-ttu-id="47030-150">**мфдесериализеаттрибутесфромстреам**</span><span class="sxs-lookup"><span data-stu-id="47030-150">**MFDeserializeAttributesFromStream**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream) |



 

<span data-ttu-id="47030-151">Чтобы записать содержимое хранилища атрибутов в массив байтов, вызовите [**мфжетаттрибутесасблоб**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob).</span><span class="sxs-lookup"><span data-stu-id="47030-151">To write the contents of an attribute store into a byte array, call [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob).</span></span> <span data-ttu-id="47030-152">Атрибуты со значениями указателей **IUnknown** игнорируются.</span><span class="sxs-lookup"><span data-stu-id="47030-152">Attributes with **IUnknown** pointer values are ignored.</span></span> <span data-ttu-id="47030-153">Чтобы загрузить атрибуты обратно в хранилище атрибутов, вызовите [**мфинитаттрибутесфромблоб**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob).</span><span class="sxs-lookup"><span data-stu-id="47030-153">To load the attributes back into an attribute store, call [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob).</span></span>

<span data-ttu-id="47030-154">Чтобы записать хранилище атрибутов в поток, вызовите [**мфсериализеаттрибутестостреам**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream).</span><span class="sxs-lookup"><span data-stu-id="47030-154">To write an attribute store to a stream, call [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream).</span></span> <span data-ttu-id="47030-155">Эта функция может маршалировать значения указателей **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="47030-155">This function can marshal **IUnknown** pointer values.</span></span> <span data-ttu-id="47030-156">Вызывающая сторона должна предоставить объект потока, реализующий интерфейс **IStream** .</span><span class="sxs-lookup"><span data-stu-id="47030-156">The caller must provide a stream object that implements the **IStream** interface.</span></span> <span data-ttu-id="47030-157">Чтобы загрузить хранилище атрибутов из потока, вызовите [**мфдесериализеаттрибутесфромстреам**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream).</span><span class="sxs-lookup"><span data-stu-id="47030-157">To load an attribute store from a stream, call [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream).</span></span>

## <a name="implementing-imfattributes"></a><span data-ttu-id="47030-158">Реализация Имфаттрибутес</span><span class="sxs-lookup"><span data-stu-id="47030-158">Implementing IMFAttributes</span></span>

<span data-ttu-id="47030-159">Media Foundation предоставляет финансовую реализацию [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), которая получается путем вызова функции [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="47030-159">Media Foundation provides a stock implementation of [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which is obtained by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span> <span data-ttu-id="47030-160">В большинстве случаев следует использовать эту реализацию и не предоставлять собственную пользовательскую реализацию.</span><span class="sxs-lookup"><span data-stu-id="47030-160">In most situations, you should use this implementation, and not provide your own custom implementation.</span></span>

<span data-ttu-id="47030-161">Существует одна ситуация, когда может потребоваться реализовать интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) : при реализации второго интерфейса, наследующего **имфаттрибутес**.</span><span class="sxs-lookup"><span data-stu-id="47030-161">There is one situation when you might need to implement the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface: If you implement a second interface that inherits **IMFAttributes**.</span></span> <span data-ttu-id="47030-162">В этом случае необходимо предоставить реализации для методов **имфаттрибутес** , наследуемых вторым интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="47030-162">In that case, you must provide implementations for the **IMFAttributes** methods inherited by the second interface.</span></span>

<span data-ttu-id="47030-163">В этом случае рекомендуется заключить существующую реализацию Media Foundation [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="47030-163">In this situation, it is recommended to wrap the existing Media Foundation implementation of [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="47030-164">В следующем коде показан шаблон класса, который содержит указатель **имфаттрибутес** и упаковывает каждый метод **имфаттрибутес** , за исключением методов **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="47030-164">The following code shows a class template that holds an **IMFAttributes** pointer and wraps every **IMFAttributes** method, except for the **IUnknown** methods.</span></span>


```C++
#include <assert.h>

// Helper class to implement IMFAttributes. 

// This is an abstract class; the derived class must implement the IUnknown 
// methods. This class is a wrapper for the standard attribute store provided 
// in Media Foundation.

// template parameter: 
// The interface you are implementing, either IMFAttributes or an interface 
// that inherits IMFAttributes, such as IMFActivate

template <class IFACE=IMFAttributes>
class CBaseAttributes : public IFACE
{
protected:
    IMFAttributes *m_pAttributes;

    // This version of the constructor does not initialize the 
    // attribute store. The derived class must call Initialize() in 
    // its own constructor.
    CBaseAttributes() : m_pAttributes(NULL)
    {
    }

    // This version of the constructor initializes the attribute 
    // store, but the derived class must pass an HRESULT parameter 
    // to the constructor.

    CBaseAttributes(HRESULT& hr, UINT32 cInitialSize = 0) : m_pAttributes(NULL)
    {
        hr = Initialize(cInitialSize);
    }

    // The next version of the constructor uses a caller-provided 
    // implementation of IMFAttributes.

    // (Sometimes you want to delegate IMFAttributes calls to some 
    // other object that implements IMFAttributes, rather than using 
    // MFCreateAttributes.)

    CBaseAttributes(HRESULT& hr, IUnknown *pUnk)
    {
        hr = Initialize(pUnk);
    }

    virtual ~CBaseAttributes()
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
        }
    }

    // Initializes the object by creating the standard Media Foundation attribute store.
    HRESULT Initialize(UINT32 cInitialSize = 0)
    {
        if (m_pAttributes == NULL)
        {
            return MFCreateAttributes(&m_pAttributes, cInitialSize); 
        }
        else
        {
            return S_OK;
        }
    }

    // Initializes this object from a caller-provided attribute store.
    // pUnk: Pointer to an object that exposes IMFAttributes.
    HRESULT Initialize(IUnknown *pUnk)
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
            m_pAttributes = NULL;
        }


        return pUnk->QueryInterface(IID_PPV_ARGS(&m_pAttributes));
    }

public:

    // IMFAttributes methods

    STDMETHODIMP GetItem(REFGUID guidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItem(guidKey, pValue);
    }

    STDMETHODIMP GetItemType(REFGUID guidKey, MF_ATTRIBUTE_TYPE* pType)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemType(guidKey, pType);
    }

    STDMETHODIMP CompareItem(REFGUID guidKey, REFPROPVARIANT Value, BOOL* pbResult)
    {
        assert(m_pAttributes);
        return m_pAttributes->CompareItem(guidKey, Value, pbResult);
    }

    STDMETHODIMP Compare(
        IMFAttributes* pTheirs, 
        MF_ATTRIBUTES_MATCH_TYPE MatchType, 
        BOOL* pbResult
        )
    {
        assert(m_pAttributes);
        return m_pAttributes->Compare(pTheirs, MatchType, pbResult);
    }

    STDMETHODIMP GetUINT32(REFGUID guidKey, UINT32* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT32(guidKey, punValue);
    }

    STDMETHODIMP GetUINT64(REFGUID guidKey, UINT64* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT64(guidKey, punValue);
    }

    STDMETHODIMP GetDouble(REFGUID guidKey, double* pfValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetDouble(guidKey, pfValue);
    }

    STDMETHODIMP GetGUID(REFGUID guidKey, GUID* pguidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetGUID(guidKey, pguidValue);
    }

    STDMETHODIMP GetStringLength(REFGUID guidKey, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetStringLength(guidKey, pcchLength);
    }

    STDMETHODIMP GetString(REFGUID guidKey, LPWSTR pwszValue, UINT32 cchBufSize, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetString(guidKey, pwszValue, cchBufSize, pcchLength);
    }

    STDMETHODIMP GetAllocatedString(REFGUID guidKey, LPWSTR* ppwszValue, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedString(guidKey, ppwszValue, pcchLength);
    }

    STDMETHODIMP GetBlobSize(REFGUID guidKey, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlobSize(guidKey, pcbBlobSize);
    }

    STDMETHODIMP GetBlob(REFGUID guidKey, UINT8* pBuf, UINT32 cbBufSize, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlob(guidKey, pBuf, cbBufSize, pcbBlobSize);
    }

    STDMETHODIMP GetAllocatedBlob(REFGUID guidKey, UINT8** ppBuf, UINT32* pcbSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedBlob(guidKey, ppBuf, pcbSize);
    }

    STDMETHODIMP GetUnknown(REFGUID guidKey, REFIID riid, LPVOID* ppv)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUnknown(guidKey, riid, ppv);
    }

    STDMETHODIMP SetItem(REFGUID guidKey, REFPROPVARIANT Value)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetItem(guidKey, Value);
    }

    STDMETHODIMP DeleteItem(REFGUID guidKey)
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteItem(guidKey);
    }

    STDMETHODIMP DeleteAllItems()
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteAllItems();
    }

    STDMETHODIMP SetUINT32(REFGUID guidKey, UINT32 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT32(guidKey, unValue);
    }

    STDMETHODIMP SetUINT64(REFGUID guidKey,UINT64 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT64(guidKey, unValue);
    }

    STDMETHODIMP SetDouble(REFGUID guidKey, double fValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetDouble(guidKey, fValue);
    }

    STDMETHODIMP SetGUID(REFGUID guidKey, REFGUID guidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetGUID(guidKey, guidValue);
    }

    STDMETHODIMP SetString(REFGUID guidKey, LPCWSTR wszValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetString(guidKey, wszValue);
    }

    STDMETHODIMP SetBlob(REFGUID guidKey, const UINT8* pBuf, UINT32 cbBufSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetBlob(guidKey, pBuf, cbBufSize);
    }

    STDMETHODIMP SetUnknown(REFGUID guidKey, IUnknown* pUnknown)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUnknown(guidKey, pUnknown);
    }

    STDMETHODIMP LockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->LockStore();
    }

    STDMETHODIMP UnlockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->UnlockStore();
    }

    STDMETHODIMP GetCount(UINT32* pcItems)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetCount(pcItems);
    }

    STDMETHODIMP GetItemByIndex(UINT32 unIndex, GUID* pguidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemByIndex(unIndex, pguidKey, pValue);
    }

    STDMETHODIMP CopyAllItems(IMFAttributes* pDest)
    {
        assert(m_pAttributes);
        return m_pAttributes->CopyAllItems(pDest);
    }

    // Helper functions
    
    HRESULT SerializeToStream(DWORD dwOptions, IStream* pStm)      
        // dwOptions: Flags from MF_ATTRIBUTE_SERIALIZE_OPTIONS
    {
        assert(m_pAttributes);
        return MFSerializeAttributesToStream(m_pAttributes, dwOptions, pStm);
    }

    HRESULT DeserializeFromStream(DWORD dwOptions, IStream* pStm)
    {
        assert(m_pAttributes);
        return MFDeserializeAttributesFromStream(m_pAttributes, dwOptions, pStm);
    }

    // SerializeToBlob: Stores the attributes in a byte array. 
    // 
    // ppBuf: Receives a pointer to the byte array. 
    // pcbSize: Receives the size of the byte array.
    //
    // The caller must free the array using CoTaskMemFree.
    HRESULT SerializeToBlob(UINT8 **ppBuffer, UINT32 *pcbSize)
    {
        assert(m_pAttributes);

        if (ppBuffer == NULL)
        {
            return E_POINTER;
        }
        if (pcbSize == NULL)
        {
            return E_POINTER;
        }

        *ppBuffer = NULL;
        *pcbSize = 0;

        UINT32 cbSize = 0;
        BYTE *pBuffer = NULL;

        HRESULT hr = MFGetAttributesAsBlobSize(m_pAttributes, &cbSize);

        if (FAILED(hr))
        {
            return hr;
        }

        pBuffer = (BYTE*)CoTaskMemAlloc(cbSize);
        if (pBuffer == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFGetAttributesAsBlob(m_pAttributes, pBuffer, cbSize);

        if (SUCCEEDED(hr))
        {
            *ppBuffer = pBuffer;
            *pcbSize = cbSize;
        }
        else
        {
            CoTaskMemFree(pBuffer);
        }
        return hr;
    }
    
    HRESULT DeserializeFromBlob(const UINT8* pBuffer, UINT cbSize)
    {
        assert(m_pAttributes);
        return MFInitAttributesFromBlob(m_pAttributes, pBuffer, cbSize);
    }

    HRESULT GetRatio(REFGUID guidKey, UINT32* pnNumerator, UINT32* punDenominator)
    {
        assert(m_pAttributes);
        return MFGetAttributeRatio(m_pAttributes, guidKey, pnNumerator, punDenominator);
    }

    HRESULT SetRatio(REFGUID guidKey, UINT32 unNumerator, UINT32 unDenominator)
    {
        assert(m_pAttributes);
        return MFSetAttributeRatio(m_pAttributes, guidKey, unNumerator, unDenominator);
    }

    // Gets an attribute whose value represents the size of something (eg a video frame).
    HRESULT GetSize(REFGUID guidKey, UINT32* punWidth, UINT32* punHeight)
    {
        assert(m_pAttributes);
        return MFGetAttributeSize(m_pAttributes, guidKey, punWidth, punHeight);
    }

    // Sets an attribute whose value represents the size of something (eg a video frame).
    HRESULT SetSize(REFGUID guidKey, UINT32 unWidth, UINT32 unHeight)
    {
        assert(m_pAttributes);
        return MFSetAttributeSize (m_pAttributes, guidKey, unWidth, unHeight);
    }
};
```



<span data-ttu-id="47030-165">В следующем коде показано, как создать класс, производный от этого шаблона:</span><span class="sxs-lookup"><span data-stu-id="47030-165">The following code shows how to derive a class from this template:</span></span>


```C++
#include <shlwapi.h>

class MyObject : public CBaseAttributes<>
{
    MyObject() : m_nRefCount(1) { }
    ~MyObject() { }

    long m_nRefCount;

public:

    // IUnknown
    STDMETHODIMP MyObject::QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(MyObject, IMFAttributes),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) MyObject::AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }

    STDMETHODIMP_(ULONG) MyObject::Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // Static function to create an instance of the object.

    static HRESULT CreateInstance(MyObject **ppObject)
    {
        HRESULT hr = S_OK;

        MyObject *pObject = new MyObject();
        if (pObject == NULL)
        {
            return E_OUTOFMEMORY;
        }

        // Initialize the attribute store.
        hr = pObject->Initialize();

        if (FAILED(hr))
        {
            delete pObject;
            return hr;
        }

        *ppObject = pObject;
        (*ppObject)->AddRef();

        return S_OK;
    }
};
```



<span data-ttu-id="47030-166">`CBaseAttributes::Initialize`Для создания хранилища атрибутов необходимо вызвать метод.</span><span class="sxs-lookup"><span data-stu-id="47030-166">You must call `CBaseAttributes::Initialize` to create the attribute store.</span></span> <span data-ttu-id="47030-167">В предыдущем примере это делается внутри функции статического создания.</span><span class="sxs-lookup"><span data-stu-id="47030-167">In the previous example, that is done inside a static creation function.</span></span>

<span data-ttu-id="47030-168">Аргумент шаблона является типом интерфейса, который по умолчанию имеет значение [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="47030-168">The template argument is an interface type, which defaults to [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="47030-169">Если объект реализует интерфейс, наследующий **имфаттрибутес**, например [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate), установите аргумент шаблона равным имени производного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="47030-169">If your object implements an interface that inherits **IMFAttributes**, such as [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate), set the template argument equal to name of the derived interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47030-170">См. также</span><span class="sxs-lookup"><span data-stu-id="47030-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47030-171">Примитивы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="47030-171">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



