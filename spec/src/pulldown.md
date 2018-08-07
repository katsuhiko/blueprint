# Group その他

## プルダウンリスト全参照 [/v1/{company_root}/pulldown]

### プルダウンリスト全参照 [GET]

* すべてのプルダウンリストを返す

+ Parameters

    + company_root: mock (string) - 個社名

+ Response 200 (application/json)

    + Attributes
        + blood (array) - 血液型
            + (object)
                + group: (string) - グループ
                + text: (string) - テキスト
                + value: (string, required) - 値
                + default: false (boolean) - 初期選択

+ Response 400 (application/json)

    + Attributes
        + message: XXXX (string, required) - エラーメッセージ
        + errors (array, required) - エラー詳細
            + (object)
                + resource:: `XX` (string, required) - resource
                + field:: `XXX` (string, required) - field
                + code:: `XXX` (string, required) - code


## プルダウンリスト参照 [/v1/{company_root}/pulldown/{item}{?group}]

### プルダウンリスト参照 [GET]

* itemのプルダウンリストを返す
* groupが空文字でない場合、絞り込みを行う（groupが一致するデータのみを返す）
* groupが空文字の場合、絞り込みを行わない

+ Parameters

    + company_root: mock (string) - 個社名
    + item: home_village (string) - プルダウンの種類指定
    + group: Asia (string) - プルダウンの絞り込み

+ Response 200 (application/json)

    + Attributes
        + blood (array) - 血液型
            + (object)
                + group: (string) - グループ
                + text: (string) - テキスト
                + value: (string, required) - 値
                + default: false (boolean) - 初期選択

+ Response 400 (application/json)

    + Attributes
        + message: XXXX (string, required) - エラーメッセージ
        + errors (array, required) - エラー詳細
            + (object)
                + resource:: `XX` (string, required) - resource
                + field:: `XXX` (string, required) - field
                + code:: `XXX` (string, required) - code
