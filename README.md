# D-META
cut_image 파일의 image_crop 함수를 사용하여
cat.jpg 이미지 파일을 2X2/3X3/3X4로 분할하였습니다.
후에 albumentations의  albumentations.HorizontalFlip(p=0.5),
                      albumentations.RandomRotate90(p=0.5),
                      albumentations.VerticalFlip(p=0.5)
 를 사용하여 각 사진을 8가지 경우의 수로 회전하도록 만들었습니다. nxm 에 대한 결과는 파일의 이름을 보시면 될 것 같습니다.

그리고 merge는 구현할 방법이 떠오르지 않았습니다. 

'merge_image를 해결하는 논리는 각 sub-image 들의 모든 edge 를 붙여보고 이들이
자연스러운지 확인되면 이들을 연결하면됩니다.
○ 중요한 두가지는 모든 edge 들을 mirroring, flipping, rotation 을 하고 붙여보는 것을
구조화해야 이를 확장할 수 있다는 것이 한가지이고, edge 를 붙인 이후에 이것이
자연스러운지에 대한 measure 를 어떻게 결정하는가 입니다.
● 불가능하다면 불가능한 이유에 대해 설명하고, 스스로 가능한 조건을 만들어서 진행하기
바랍니다.'

이 말에 대해 80%  이해할 수는 있겠는데 , '자연스러운지'에서 이 자연스러움을 어떠한 지표를 사용하여 판단할지 의문이었고
사진들을 다 붙여봐서 구조화하는 것도 제게 어려운 일이었습니다.
일단 이러한 코딩 테스트 유형을 처음 겪어봐서 (저는 백준, 프로그래머스만 풀어봤습니다.) 당황하기도하고 어렵기도 했으나 제가 할 수 있는 최선은 다 했다고 생각합니다.

