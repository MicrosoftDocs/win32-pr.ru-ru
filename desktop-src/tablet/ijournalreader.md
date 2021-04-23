---
description: Предоставляет доступ на чтение к файлу журнала Windows, возвращая поток, содержащий XML-версию содержимого файла.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: Интерфейс Ижаурналреадер (журнал. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 7576996d341f13518879310f08c0a48996e1293f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349912"
---
# <a name="ijournalreader-interface"></a><span data-ttu-id="01c14-103">Интерфейс Ижаурналреадер</span><span class="sxs-lookup"><span data-stu-id="01c14-103">IJournalReader interface</span></span>

<span data-ttu-id="01c14-104">Предоставляет доступ на чтение к файлу журнала Windows, возвращая поток, содержащий XML-версию содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="01c14-104">Provides read access to a Windows Journal file, returning a stream containing an XML version of the file's contents.</span></span>

> [!Note]  
> <span data-ttu-id="01c14-105">Компоненту чтения журнала не удается прочитать файлы журнала Windows, созданные на компьютерах под управлением Windows 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="01c14-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="01c14-106">Интерфейс Ижаурналреадер должен считаться устаревшим или устаревшим и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="01c14-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="members"></a><span data-ttu-id="01c14-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="01c14-107">Members</span></span>

<span data-ttu-id="01c14-108">Интерфейс **ижаурналреадер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="01c14-108">The **IJournalReader** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="01c14-109">**Ижаурналреадер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="01c14-109">**IJournalReader** also has these types of members:</span></span>

-   [<span data-ttu-id="01c14-110">Методы</span><span class="sxs-lookup"><span data-stu-id="01c14-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="01c14-111">Методы</span><span class="sxs-lookup"><span data-stu-id="01c14-111">Methods</span></span>

<span data-ttu-id="01c14-112">Интерфейс **ижаурналреадер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="01c14-112">The **IJournalReader** interface has these methods.</span></span>



| <span data-ttu-id="01c14-113">Метод</span><span class="sxs-lookup"><span data-stu-id="01c14-113">Method</span></span>                                                  | <span data-ttu-id="01c14-114">Описание</span><span class="sxs-lookup"><span data-stu-id="01c14-114">Description</span></span>                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01c14-115">**реадфромстреам**</span><span class="sxs-lookup"><span data-stu-id="01c14-115">**ReadFromStream**</span></span>](ijournalreader-readfromstream.md) | <span data-ttu-id="01c14-116">Принимает поток в файл заметки журнала и возвращает XML-поток, представляющий содержимое документа.</span><span class="sxs-lookup"><span data-stu-id="01c14-116">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="01c14-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01c14-117">Remarks</span></span>

<span data-ttu-id="01c14-118">Класс **жаурналреадер** позволяет загрузить поток документа журнала и получить XML-поток, представляющий содержимое.</span><span class="sxs-lookup"><span data-stu-id="01c14-118">The **JournalReader** class enables you to load a Journal document stream and to receive an XML stream representing the contents.</span></span> <span data-ttu-id="01c14-119">Вы можете воспроизводить, отображать и манипулировать рукописными данными.</span><span class="sxs-lookup"><span data-stu-id="01c14-119">You can reconstitute, display, and manipulate the ink.</span></span>

## <a name="examples"></a><span data-ttu-id="01c14-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="01c14-120">Examples</span></span>

<span data-ttu-id="01c14-121">Следующий пример обработчика для события [**нажатия**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) кнопки создает экземпляр класса **жаурналреадер** и использует его для чтения существующего файла журнала.</span><span class="sxs-lookup"><span data-stu-id="01c14-121">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the **JournalReader** class and uses it to read an existing Journal file.</span></span>

> [!Note]  
> <span data-ttu-id="01c14-122">Метод **дисплайксмл** , вызываемый из этого примера, не показан.</span><span class="sxs-lookup"><span data-stu-id="01c14-122">The **DisplayXml** method called from this example is not shown.</span></span> <span data-ttu-id="01c14-123">Конкретная реализация такого метода зависит от потребностей вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="01c14-123">The specific implementation of such a method is dependent on your application's needs.</span></span>

 


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  static TCHAR BASED_CODE szFilter[] = 
    _T("Journal files (*.jnt)|*.jnt|All files (*.*)|*.*");
  CFileDialog* fileDialog = new CFileDialog(TRUE, _T("*.jnt"), NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user via a File Open dialog
  if (fileDialog != NULL &&
      fileDialog->DoModal() == IDOK)
  {
    CString strFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(strFileName,
                              GENERIC_READ,
                              FILE_SHARE_READ,
                              NULL,
                              OPEN_EXISTING,
                              FILE_ATTRIBUTE_NORMAL,
                              NULL);
    
    if (hFile != INVALID_HANDLE_VALUE)
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
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) &&
              (dwRead == dwFileSize))
          {
            HRESULT hr;
            IStream* pJntStream;

            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              IJournalReader* pJntReader;

              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                IStream* pXmlStream;

                // Read in the JNT file via the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                if (SUCCEEDED(hr))
                {
                  // Display results
                  DisplayXml(pXmlStream);

                  // Clean up
                  pXmlStream->Release();
                }
                pJntReader->Release();
              }
              pJntStream->Release();
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
      CloseHandle(hFile);
    }
    delete fileDialog;
  }
}
```



## <a name="requirements"></a><span data-ttu-id="01c14-124">Требования</span><span class="sxs-lookup"><span data-stu-id="01c14-124">Requirements</span></span>



| <span data-ttu-id="01c14-125">Требование</span><span class="sxs-lookup"><span data-stu-id="01c14-125">Requirement</span></span> | <span data-ttu-id="01c14-126">Значение</span><span class="sxs-lookup"><span data-stu-id="01c14-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c14-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01c14-127">Minimum supported client</span></span><br/> | <span data-ttu-id="01c14-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="01c14-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="01c14-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01c14-129">Minimum supported server</span></span><br/> | <span data-ttu-id="01c14-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="01c14-130">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="01c14-131">Header</span><span class="sxs-lookup"><span data-stu-id="01c14-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="01c14-132"><dt>Журнал. h (также требуется журнал \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="01c14-132"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="01c14-133">DLL</span><span class="sxs-lookup"><span data-stu-id="01c14-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01c14-134"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01c14-134"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="01c14-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01c14-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c14-136">Идентификаторы GUID настраиваемых свойств</span><span class="sxs-lookup"><span data-stu-id="01c14-136">Custom Property GUIDs</span></span>](custom-property-guids.md)
</dt> <dt>

[<span data-ttu-id="01c14-137">**Метод Реадфромстреам**</span><span class="sxs-lookup"><span data-stu-id="01c14-137">**ReadFromStream Method**</span></span>](ijournalreader-readfromstream.md)
</dt> </dl>

 

