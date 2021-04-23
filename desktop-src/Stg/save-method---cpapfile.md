---
title: Метод Save — Кпапфиле
description: При инициализации Кпапфиле его можно использовать для сохранения текущих данных, хранящихся в объекте-документе.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- Метод Save — Кпапфиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986854"
---
# <a name="save-method---cpapfile"></a><span data-ttu-id="5cc8c-104">Метод Save — Кпапфиле</span><span class="sxs-lookup"><span data-stu-id="5cc8c-104">Save Method - CPapFile</span></span>

<span data-ttu-id="5cc8c-105">При инициализации **кпапфиле** его можно использовать для сохранения текущих данных, хранящихся в объекте-документе.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-105">When **CPapFile** is initialized, it can be used to save the current drawing data held in the COPaper object.</span></span>

## <a name="save-method-papfilecpp"></a><span data-ttu-id="5cc8c-106">Метод Save (ПАПФИЛЕ. CPP</span><span class="sxs-lookup"><span data-stu-id="5cc8c-106">Save Method (PAPFILE.CPP)</span></span>

<span data-ttu-id="5cc8c-107">В этом примере используется метод  [**Save**](ipaper--save.md) **кпапфиле** из папфиле. cpp.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-107">This example is the **CPapFile** [**Save**](ipaper--save.md) method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



<span data-ttu-id="5cc8c-108">Если для параметра *pszFileName* передается **значение NULL** , в качестве имени файла используется сохраненное содержимое члена **m \_ сзкурфиленаме** .</span><span class="sxs-lookup"><span data-stu-id="5cc8c-108">If **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="5cc8c-109">*Нлокккэй* — это ключ блокировки клиента, полученный в предыдущем вызове метода [**блокировки**](ipaper-methods.md) собумаги в интерфейсе **ипапер** .</span><span class="sxs-lookup"><span data-stu-id="5cc8c-109">The *nLockKey* is the client lock key obtained in a previous call to the COPaper [**Lock**](ipaper-methods.md) method in the **IPaper** interface.</span></span>

<span data-ttu-id="5cc8c-110">Функция службы COM Standard [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) вызывается для создания составного файла, в котором будут сохранены данные рисования.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-110">The COM standard [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) service function is called to create the compound file in which the drawing data will be saved.</span></span>

<span data-ttu-id="5cc8c-111">Имя создаваемого составного файла передается как первый параметр.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-111">The name of the compound file to create is passed as the first parameter.</span></span> <span data-ttu-id="5cc8c-112">Ожидается, что [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) в виде строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-112">This is expected by [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as a Unicode string.</span></span> <span data-ttu-id="5cc8c-113">Когда **стоклиен** компилируется для строк ANSI (Юникод не определен, что является значением по умолчанию в файле Makefile), этот вызов фактически сокращается до вызова внутренней функции аппутил, **\_ стгкреатедокфиле**.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-113">When **StoClien** is compiled for ANSI strings (UNICODE is not defined, which is the default in the makefile), this call actually reduces to a call to an internal APPUTIL function, **A\_StgCreateDocfile**.</span></span> <span data-ttu-id="5cc8c-114">Эта функция выполняет правильное преобразование параметра Псзфиле ANSI в версию Юникода перед вызовом **стгкреатедокфиле**.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-114">This function performs the proper conversion of the ANSI pszFile parameter to a Unicode version before calling **StgCreateDocfile**.</span></span> <span data-ttu-id="5cc8c-115">Дополнительные сведения см. в разделе Аппутил. h и Stoserve.htm.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-115">For more information, see Apputil.h and Stoserve.htm.</span></span>

<span data-ttu-id="5cc8c-116">Флаги режима доступа передаются в качестве второго параметра и определяют, какие режимы доступа разрешены для нового файла.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-116">The access mode flags are passed as the second parameter and determine which access modes are permitted on the new file.</span></span> <span data-ttu-id="5cc8c-117">Флаг [ \_ создания](stgm-constants.md) режима доступа стгм создает новый составной файл или перезаписывает существующий с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-117">The [STGM\_CREATE](stgm-constants.md) access mode flag creates a new compound file or overwrites an existing one of the same name.</span></span> <span data-ttu-id="5cc8c-118">[Стгм \_ READWRITE](stgm-constants.md) открывает файл с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-118">[STGM\_READWRITE](stgm-constants.md) opens the file with read-write permission.</span></span> <span data-ttu-id="5cc8c-119">[Стгм \_ DIRECT](stgm-constants.md) открывает файл для прямого доступа в отличие от транзакционного доступа.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-119">[STGM\_DIRECT](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="5cc8c-120">[Стгм \_ \_Монопольный доступ](stgm-constants.md) открывает файл для монопольного использования, не являющегося общим для вызывающего.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-120">[STGM\_SHARE\_EXCLUSIVE](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="5cc8c-121">Третий параметр зарезервирован и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-121">The third parameter is reserved and must be zero.</span></span>

<span data-ttu-id="5cc8c-122">Адрес переменной указателя **m \_ пистораже** передается в [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) в качестве четвертого параметра.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-122">The address of pointer variable **m\_pIStorage** is passed to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as the fourth parameter.</span></span> <span data-ttu-id="5cc8c-123">Когда вызов успешно возвращается, **m \_ пистораже** содержит указатель интерфейса на интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="5cc8c-123">When the call successfully returns, **m\_pIStorage** contains an interface pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="5cc8c-124">Это интерфейс, который используется для последующих операций с файлом.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-124">This is the interface that is used for any subsequent operations on the file.</span></span>

<span data-ttu-id="5cc8c-125">Важной операцией в этом случае является то, что объект собумага сохраняет данные рисования в файле.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-125">The important operation in this case is to have the COPaper object store its drawing data in the file.</span></span> <span data-ttu-id="5cc8c-126">Это делается с помощью метода [**Save**](ipaper--save.md) интерфейса [**ипапер**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc8c-126">This is done above using the [**Save**](ipaper--save.md) method of the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="5cc8c-127">Если относительная бумага будет сохранена в предоставленном объекте хранилища, имя составного файла будет скопировано в **\_ сзкурфиленаме m** в качестве нового имени текущего файла.</span><span class="sxs-lookup"><span data-stu-id="5cc8c-127">If COPaper succeeds in saving its data in the storage object provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

 

 




