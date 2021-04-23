---
description: Принимает поток в файл заметки журнала и возвращает XML-поток, представляющий содержимое документа.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: 'Метод Ижаурналреадер:: Реадфромстреам (журнал. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader.ReadFromStream
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 258ac30b8857fa4ef24bd86a08c7e402229f4bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692156"
---
# <a name="ijournalreaderreadfromstream-method"></a><span data-ttu-id="33fb1-103">Метод Ижаурналреадер:: Реадфромстреам</span><span class="sxs-lookup"><span data-stu-id="33fb1-103">IJournalReader::ReadFromStream method</span></span>

<span data-ttu-id="33fb1-104">Принимает поток в файл заметки журнала и возвращает XML-поток, представляющий содержимое документа.</span><span class="sxs-lookup"><span data-stu-id="33fb1-104">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span>

> [!Note]  
> <span data-ttu-id="33fb1-105">Компоненту чтения журнала не удается прочитать файлы журнала Windows, созданные на компьютерах под управлением Windows 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="33fb1-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="33fb1-106">Интерфейс Ижаурналреадер должен считаться устаревшим или устаревшим и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="33fb1-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="33fb1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33fb1-107">Syntax</span></span>


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a><span data-ttu-id="33fb1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="33fb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33fb1-109">*пжаурналфилестреам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="33fb1-109">*pJournalFileStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33fb1-110">Объект [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , представляющий файл журнала для чтения.</span><span class="sxs-lookup"><span data-stu-id="33fb1-110">An [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object representing the Journal file to read.</span></span>

</dd> <dt>

<span data-ttu-id="33fb1-111">*ппксмлстреам* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="33fb1-111">*ppXmlStream* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="33fb1-112">Указатель на адрес объекта [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , который получит XML-поток, созданный при чтении файла журнала.</span><span class="sxs-lookup"><span data-stu-id="33fb1-112">A pointer to the address of an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object that will receive the XML stream created by reading the Journal file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33fb1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33fb1-113">Return value</span></span>

<span data-ttu-id="33fb1-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="33fb1-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33fb1-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33fb1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="33fb1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33fb1-116">Remarks</span></span>

<span data-ttu-id="33fb1-117">Потоки используются для предотвращения прямого доступа к файловой системе и для выбора метода синтаксического анализа XML.</span><span class="sxs-lookup"><span data-stu-id="33fb1-117">Streams are used to avoid direct access to the file system and to allow choice in which XML parsing method to use.</span></span>

## <a name="examples"></a><span data-ttu-id="33fb1-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="33fb1-118">Examples</span></span>

<span data-ttu-id="33fb1-119">Следующий пример обработчика для события [**нажатия**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) кнопки создает экземпляр интерфейса [**интерфейса ижаурналреадер**](ijournalreader.md) и использует его для чтения существующего файла журнала.</span><span class="sxs-lookup"><span data-stu-id="33fb1-119">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the [**IJournalReader Interface**](ijournalreader.md) interface and uses it to read an existing Journal file.</span></span>


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  IStream* pJntStream;
  IStream* pXmlStream;
  IJournalReader* pJntReader;
  HRESULT hr;
  CString szFileName = "";
  static char BASED_CODE szFilter[] = 
    "Journal files (*.jnt)|*.jnt|All files (*.*)|*.*";
  CFileDialog* fileDialog = new CFileDialog(TRUE, "*.jnt", NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user by using a File Open dialog
  if (IDOK == fileDialog->DoModal())
  {
    szFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(szFileName.GetBuffer(), GENERIC_READ, FILE_SHARE_READ, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    
    if (INVALID_HANDLE_VALUE != hFile)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) && dwRead == dwFileSize)
          {
            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                // Read in the JNT file by using the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                // Display results
                if (SUCCEEDED(hr))
                {
                  DisplayXml(pXmlStream);
                }

                // Clean up
                pXmlStream->Release();
                pJntReader = NULL;
                pJntStream->Release();
              }
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
    }
  }
}
```



## <a name="requirements"></a><span data-ttu-id="33fb1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="33fb1-120">Requirements</span></span>



| <span data-ttu-id="33fb1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="33fb1-121">Requirement</span></span> | <span data-ttu-id="33fb1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="33fb1-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33fb1-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33fb1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="33fb1-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="33fb1-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33fb1-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33fb1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="33fb1-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="33fb1-126">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="33fb1-127">Header</span><span class="sxs-lookup"><span data-stu-id="33fb1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="33fb1-128"><dt>Журнал. h (также требуется журнал \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="33fb1-128"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="33fb1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="33fb1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33fb1-130"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33fb1-130"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="33fb1-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33fb1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33fb1-132">**Интерфейс Ижаурналреадер**</span><span class="sxs-lookup"><span data-stu-id="33fb1-132">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="33fb1-133">Справочник по схеме чтения журнала</span><span class="sxs-lookup"><span data-stu-id="33fb1-133">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

