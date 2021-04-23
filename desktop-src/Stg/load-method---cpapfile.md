---
title: Метод Load — Кпапфиле
description: После успешного выполнения этих операций полученный интерфейс IStorage освобождается. Этот файл закрывается и указывает, что файл не удерживается открытым во время других операций клиента. Он будет открыт повторно при необходимости.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Метод Load — Кпапфиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889240"
---
# <a name="load-method---cpapfile"></a><span data-ttu-id="95f97-106">Метод Load — Кпапфиле</span><span class="sxs-lookup"><span data-stu-id="95f97-106">Load Method - CPapFile</span></span>

<span data-ttu-id="95f97-107">После успешного выполнения этих операций полученный интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) освобождается.</span><span class="sxs-lookup"><span data-stu-id="95f97-107">When these operations are successful, the obtained [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface is released.</span></span> <span data-ttu-id="95f97-108">Этот файл закрывается и указывает, что файл не удерживается открытым во время других операций клиента.</span><span class="sxs-lookup"><span data-stu-id="95f97-108">This closes the file and indicates that the file is not held open during other client operations.</span></span> <span data-ttu-id="95f97-109">Он будет открыт повторно при необходимости.</span><span class="sxs-lookup"><span data-stu-id="95f97-109">It will be reopened when required.</span></span>

<span data-ttu-id="95f97-110">В этом примере используется метод  **Load** **кпапфиле** из папфиле. cpp.</span><span class="sxs-lookup"><span data-stu-id="95f97-110">This example is the **CPapFile** **Load** method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a><span data-ttu-id="95f97-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95f97-111">Remarks</span></span>

<span data-ttu-id="95f97-112">Как и при использовании метода [**Save**](save-method---cpapfile.md) , если для параметра *pszFileName* передается **значение NULL** , в качестве имени файла используется сохраненное содержимое члена **m \_ сзкурфиленаме** .</span><span class="sxs-lookup"><span data-stu-id="95f97-112">As with the [**Save**](save-method---cpapfile.md) method, if **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="95f97-113">Поскольку существующий файл может быть открыт, функция АППУТИЛ **филиксист** сначала используется для проверки существования файла.</span><span class="sxs-lookup"><span data-stu-id="95f97-113">Because an existing file may be opened, the APPUTIL **FileExist** function is first used to verify that the file exists.</span></span> <span data-ttu-id="95f97-114">Если он существует, вызывается Стандартная функция [**стгиссторажефиле**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) Service для проверки формата файла, чтобы определить, является ли он допустимым составным файлом.</span><span class="sxs-lookup"><span data-stu-id="95f97-114">If it exists, the standard [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) service function is called to verify the format of the file to determine if it is a valid compound file.</span></span>

<span data-ttu-id="95f97-115">Если файл является допустимым, вызывается Стандартная функция [**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) Service, чтобы открыть файл и вернуть указатель на интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) для него.</span><span class="sxs-lookup"><span data-stu-id="95f97-115">If the file is valid, the standard [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) service function is called to open the file and return a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for it.</span></span>

<span data-ttu-id="95f97-116">Первый параметр — это имя создаваемого составного файла.</span><span class="sxs-lookup"><span data-stu-id="95f97-116">The first parameter is the name of the compound file to open.</span></span> <span data-ttu-id="95f97-117">Как и при вызове [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , эта строка ожидается в форме Юникода, и во время компиляции ANSI макрос аппутил используется для преобразования параметра ANSI в ожидаемый символ Юникода.</span><span class="sxs-lookup"><span data-stu-id="95f97-117">As with the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) call, this string is expected in the Unicode form, and during ANSI compilation an APPUTIL macro is used to ensure the ANSI parameter is converted to the expected Unicode.</span></span>

<span data-ttu-id="95f97-118">Второй параметр хранилища с приоритетом имеет **значение NULL**, что означает, что он не используется в этом примере.</span><span class="sxs-lookup"><span data-stu-id="95f97-118">The second priority storage parameter is **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="95f97-119">Флаги режима доступа передаются в качестве третьего параметра, чтобы указать, какие режимы доступа разрешены для открытого файла.</span><span class="sxs-lookup"><span data-stu-id="95f97-119">The access mode flags are passed as the third parameter to specify what access modes are permitted on the opened file.</span></span> <span data-ttu-id="95f97-120">[**Стгм \_ READ**](stgm-constants.md) открывает файл с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="95f97-120">[**STGM\_READ**](stgm-constants.md) opens the file with read-only permission.</span></span> <span data-ttu-id="95f97-121">[**Стгм \_ DIRECT**](stgm-constants.md) открывает файл для прямого доступа в отличие от транзакционного доступа.</span><span class="sxs-lookup"><span data-stu-id="95f97-121">[**STGM\_DIRECT**](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="95f97-122">[**Стгм \_ \_Монопольный доступ**](stgm-constants.md) открывает файл для монопольного использования, не являющегося общим для вызывающего.</span><span class="sxs-lookup"><span data-stu-id="95f97-122">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="95f97-123">Четвертый параметр исключения элемента в **значении NULL**, указывающий, что он не используется в этом примере.</span><span class="sxs-lookup"><span data-stu-id="95f97-123">The fourth element exclusion parameter in **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="95f97-124">Пятый параметр зарезервирован для будущего использования и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="95f97-124">The fifth parameter is reserved for future use and must be zero.</span></span>

<span data-ttu-id="95f97-125">Адрес переменной указателя **m \_ пистораже** передается в качестве шестого параметра.</span><span class="sxs-lookup"><span data-stu-id="95f97-125">The address of pointer variable **m\_pIStorage** is passed as the sixth parameter.</span></span> <span data-ttu-id="95f97-126">Когда вызов завершается успешно, **m \_ пистораже** содержит указатель на интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="95f97-126">When the call successfully returns, **m\_pIStorage** contains a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="95f97-127">Это интерфейс, который используется для последующих операций с открытым файлом.</span><span class="sxs-lookup"><span data-stu-id="95f97-127">This is the interface that is used for any subsequent operations on the opened file.</span></span>

<span data-ttu-id="95f97-128">Важной операцией в этом случае является то, что объект собумага загружает данные рисования из файла.</span><span class="sxs-lookup"><span data-stu-id="95f97-128">The important operation in this case is to have the COPaper object load its drawing data from the file.</span></span> <span data-ttu-id="95f97-129">Это делается с помощью метода **Load** интерфейса [**ипапер**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="95f97-129">This is done above using the **Load** method of COPaper's [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="95f97-130">Если собумага завершила загрузку своих данных с помощью предоставленного [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , имя составного файла копируется в **m \_ сзкурфиленаме** в качестве нового имени текущего файла.</span><span class="sxs-lookup"><span data-stu-id="95f97-130">If COPaper succeeds in loading its data using the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

<span data-ttu-id="95f97-131">После успешного выполнения этих операций полученный интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) освобождается.</span><span class="sxs-lookup"><span data-stu-id="95f97-131">When these operations are successfully completed, the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface that was obtained is released.</span></span> <span data-ttu-id="95f97-132">Этот файл закрывается и означает, что файл не удерживается открытым во время других операций клиента.</span><span class="sxs-lookup"><span data-stu-id="95f97-132">This closes the file and means that the file is not held open during other client operations.</span></span> <span data-ttu-id="95f97-133">Он будет открыт повторно при необходимости.</span><span class="sxs-lookup"><span data-stu-id="95f97-133">It will be reopened when required.</span></span>

 

 




