---
description: загрузка Graph из внешнего процесса
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: загрузка Graph из внешнего процесса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e92fdaebb9ce3cb6615153daf66a8991477bf76e16ac3298e8e8b2fb59d74b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831063"
---
# <a name="loading-a-graph-from-an-external-process"></a>загрузка Graph из внешнего процесса

Графедит может загрузить граф фильтра, созданный внешним процессом. С помощью этой функции можно увидеть, какой граф фильтра создает приложение, с минимальным объемом дополнительного кода в приложении.

> [!Note]  
> для этого компонента требуется Windows 2000, Windows XP или более поздней версии.

 

> [!Note]  
> начиная с Windows Vista необходимо зарегистрировать proppage.dll, чтобы включить эту функцию. Proppage.dll входит в Windows SDK.

 

Приложение должно зарегистрировать экземпляр графа фильтра в запущенной таблице объектов (ROT). ROT — это глобально доступная Таблица поиска, которая отслеживает выполняемые объекты. Объекты регистрируются в таблице ROT с помощью моникера. Чтобы подключиться к графу, Графедит выполняет поиск моникеров в таблице ROT, отображаемое имя которых соответствует определенному формату:


```C++
!FilterGraph X pid Y
```



где *X* — шестнадцатеричный адрес фильтра Graph Manager, а *Y* — идентификатор процесса, также в шестнадцатеричном формате.

Когда приложение сначала создает граф фильтра, вызовите следующую функцию:


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



Эта функция создает моникер и новую запись ROT для графа фильтра. Первый параметр — это указатель на граф фильтра. Второй параметр получает значение, идентифицирующее новую запись ROT. Прежде чем приложение выпустит граф фильтра, вызовите следующую функцию, чтобы удалить запись ROT. Параметр *пдврегистер* — это идентификатор, возвращаемый функцией аддторот.


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



В следующем примере кода показано, как вызывать эти функции. В этом примере код, который добавляет и удаляет записи ROT, компилируется условно, так что он включается только в отладочных сборках.


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



Чтобы просмотреть граф фильтра в Графедит, запустите приложение и Графедит в то же время. в меню графедит **File (файл файла** ) выберите пункт **Подключение to Remote Graph...** в диалоговом окне **Подключение To Graph** выберите идентификатор процесса (pid) приложения и нажмите кнопку **ок**. Графедит загружает граф фильтра и отображает его. Не используйте другие функции Графедит на этом графе — это может привести к непредвиденным результатам. Например, не добавляйте и не удаляйте фильтры, а также приостанавливаете и запускаете граф. Перед выходом из приложения закройте Графедит.

> [!Note]  
> Приложение может столкнуться с различными утверждениями при его выходе. На них можно не обращать внимания.

 

на следующем рисунке показано диалоговое окно **Подключение To Graph** .

![подключение к графу](images/gedit-spy.png)

Когда Графедит загружает граф, он выполняется в контексте целевого приложения. Таким образом, Графедит может блокироваться, так как ожидает поток. Например, это может произойти при пошаговом выполнении кода в отладчике.

Эта функция должна использоваться только в отладочных сборках приложения, а не в розничных сборках, так как позволяет другим приложениям просматривать граф фильтра и управлять им.

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a>подключение к удаленному Graph из командной строки

Графедит поддерживает параметр командной строки для автоматической загрузки удаленного графа при запуске. Синтаксис:


```C++
GraphEdt -a moniker
```



где *моникер* — моникер, созданный с помощью функции аддторот, описанной выше.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[имитация Graph сборки с помощью графедит](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



